# System Requirements

#### JFrog Version Support  <a href="#jfrog-version-support" id="jfrog-version-support"></a>

| Artifactory | Xray    |
| ----------- | ------- |
| 7.77.20     | 3.104.8 |

#### Computing Platforms Support  <a href="#computing-platforms-support" id="computing-platforms-support"></a>

| AWS                                                                                                                                 | GCP                                                                                                                                 | Azure                                                                                                                               | On-prem Kubernetes                                                                                                                  |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) |

#### Containers Technology Support  <a href="#containers-technology-support" id="containers-technology-support"></a>

| Kubernetes | OpenShift                                                                                                                           |
| ---------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| 1.21+      | ![:cross\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-cross\_mark/path) |

#### Kernel Operating Systems Support  <a href="#kernel-operating-systems-support" id="kernel-operating-systems-support"></a>

| Linux Kernel         | Windows Kernel                                                                                                                      |
| -------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| <p>4.18+</p><p> </p> | ![:cross\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-cross\_mark/path) |

#### Supported Node Architecture  <a href="#supported-node-architecture" id="supported-node-architecture"></a>

| X86-64                                                                                                                              | ARM64                                                                                                                               |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) |

#### CPU and Memory <a href="#cpu-and-memory" id="cpu-and-memory"></a>

Nodes are considered to run an average of 100 pods.

| Number of running nodes | CPU                                            | Memory  |
| ----------------------- | ---------------------------------------------- | ------- |
| 100 nodes and below     | 6 Cores                                        | 10 GiB  |
| 500 nodes and below     | 30 Cores                                       | 50 GiB  |
| 1000 nodes and below    | 60 Cores                                       | 100 GiB |
| 1500 nodes and below    | 90 Cores                                       | 150 GiB |
| 2000 nodes and below    | 120 Cores                                      | 200 GiB |
| 2000 and above          | Contact JFrog Support for sizing requirements. |         |

&#x20;

#### **Runtime Impact - Recommended Postgres Database** <a href="#runtime-impact-recommended-postgres-database" id="runtime-impact-recommended-postgres-database"></a>

Type of supported database: Postgres16

Nodes are considered to run an average of 100 pods.

| Monitored Nodes                                                  | vCPUs                                          | Memory (GiB) | Storage Type                                                        | Network Performance |
| ---------------------------------------------------------------- | ---------------------------------------------- | ------------ | ------------------------------------------------------------------- | ------------------- |
| Runtime Integrity (controller only setup) or 100 nodes and below | 2                                              | 10           | <p>SSD</p><p>20 GiB<br>IOps: 600<br>Throughput:500MBps</p>          | 4750 Mbps           |
| 500 nodes and below                                              | 10                                             | 32           | <p>SSD</p><p>100 GiB</p><p>IOps: 3000</p><p>Throughput:500MBps</p>  | 4750 Mbps           |
| 1000 nodes and below                                             | 20                                             | 64           | <p>SSD</p><p>200 GiB</p><p>IOps: 6000</p><p>Throughput:500MBps</p>  | 4750 Mbps           |
| 1500 nodes and below                                             | 30                                             | 96           | <p>SSD</p><p>300 GiB</p><p>IOps: 9000</p><p>Throughput:500MBps</p>  | 9600 Mbps           |
| 2000 nodes and below                                             | 40                                             | 128          | <p>SSD</p><p>400 GiB</p><p>IOps: 12000</p><p>Throughput:700MBps</p> | 9600 Mbps           |
| 2000 nodes and above                                             | Contact JFrog Support for sizing requirements. |              |                                                                     |                     |

#### Supported Package Types <a href="#supported-package-type" id="supported-package-type"></a>

| Java                                                                                                                                | Go                                                                                                                                  | OS executables                                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) |

&#x20;
