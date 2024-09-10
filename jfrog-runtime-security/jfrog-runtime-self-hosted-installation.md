# JFrog Runtime Self-Hosted Installation

To follow this guide, make sure your `kubectl` and `helm` clients can access the Kubernetes cluster where you want to install the Runtime Service.

In addition, you will need an ingress controller (preferably configured with TLS).\
We officially support only the Nginx controller, but it can work with any ingress controller that supports gRPC traffic.

### Install JFrog Platform

#### **JFrog Charts**

For the installation of the different JFrog Platform components, you will need access to the JFrog Charts Repository. \
Add and update the JFrog Helm Chart repository in your local configuration:\
`helm repo add jfrog https://charts.jfrog.io --force-update`

To view the general JFrog Platform installation steps, see [here](https://jfrog.com/help/r/jfrog-installation-setup-documentation/install).&#x20;

#### **Artifactory Installation**

Make some small adjustments to the values of Artifactory, as follows:

To view the general Artifactory installation steps, see [here](https://jfrog.com/help/r/jfrog-installation-setup-documentation/installing-artifactory).&#x20;

```
# This is related to a standalone nginx server, as opposed to an ingress-controller.
nginx:
  enabled: false
ingress:
  enabled: true
  defaultBackend:
    enabled: true
  hosts:
    # This should be set to a domain which is associated with the 
    # external IPs of your ingress load balancer.
    - <add-your-public-domain-here>
  routerPath: /
  disableRouterBypass: true
  artifactoryPath: /artifactory/
  className: "nginx"
  annotations:
    nginx.ingress.kubernetes.io/proxy-read-timeout: "600"
    nginx.ingress.kubernetes.io/proxy-send-timeout: "600"
    nginx.ingress.kubernetes.io/proxy-body-size: "0"
    nginx.ingress.kubernetes.io/rewrite-target: "/"
  tls:
    - secretName: artifactory-tls-secret
      hosts:
        # This should be set to a domain which is associated with the 
        # external IPs of your ingress load balancer.
        - <add-your-public-domain-here>
```

### Install the Runtime Service

As with Artifactory and Xray, install the Runtime Service using Helm

Create a new file named `runtime-values.yaml` with the following content:

```
global:
  deployEnv: onprem
  
  # This should be set to a domain which is associated with the 
  # external IPs of your ingress load balancer.

  jfrogUrl: <add-your-public-domain-here>

postgresql:
  enabled: true

# To use external database:
# database:
#   url: postgres://<host>:5432/runtime
#   user: runtime
#   password: <password>

ingress:
  grpc:
    tlsSecretName: runtime-tls-secret
    securedBackendProtocol: false

router:
  jfrogUrl: <artifactory-service-url> # http://artifactory:8082

runtime:
  joinKey: <join-key> # The same one from artifactory
  image:
    registry: releases-docker.jfrog.io
```

Run the following to install the runtime service:

```
helm upgrade --install runtime -f runtime-values.yaml
```

### Install Runtime Sensors

To obtain the installation snippet for runtime sensors, navigate to Artifactoy > Administration > Runtime Settings > Sensor Management, and click the Install Runtime button to open the sensor installation wizard. For more information, see [Controller/Sensor Installation](../sensor-management/controller-sensor-installation/).&#x20;

#### **Bypassing Certificate Verification**

If you’re using a self-signed certificate, you must configure the sensors to bypass verification of the server's certificate chain and hostname. To apply this configuration, set the following value in the sensor installation snippet you copied from the sensor installation wizard:\
`--set tlsInsecureSkipVerify=true`

Note that this setup should be carefully reconsidered for production environments based on your organization’s security requirements and constraints.
