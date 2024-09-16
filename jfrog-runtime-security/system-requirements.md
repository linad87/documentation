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

| Number of running nodes | CPU                                            | Memory |
| ----------------------- | ---------------------------------------------- | ------ |
| 100 nodes and below     | 6 Cores                                        | 16 GiB |
| 500 nodes and below     | 30 Cores                                       | 16 GiB |
| 1000 nodes and below    | Contact JFrog Support for sizing requirements. |        |

&#x20;

#### **Runtime Impact - Recommended Postgres Database** <a href="#runtime-impact-recommended-postgres-database" id="runtime-impact-recommended-postgres-database"></a>

Type of supported database: Postgres16

Nodes are considered to run an average of 100 pods.

<table><thead><tr><th>Monitored Nodes</th><th width="200">vCPUs</th><th>Memory (GiB)</th><th>Storage Type</th><th>Network Performance</th></tr></thead><tbody><tr><td>Runtime Integrity (controller only setup) or 100 nodes and below</td><td>2</td><td>10</td><td><p>SSD</p><p>20 GiB<br>IOps: 600<br>Throughput:500MBps</p></td><td>4750 Mbps</td></tr><tr><td>500 nodes and below</td><td>10</td><td>32</td><td><p>SSD</p><p>100 GiB</p><p>IOps: 3000</p><p>Throughput:500MBps</p></td><td>4750 Mbps</td></tr><tr><td>1000 nodes and below</td><td>Contact JFrog Support for sizing requirements.</td><td></td><td></td><td></td></tr></tbody></table>

#### Runtime Impact Supported Package Types <a href="#supported-package-type" id="supported-package-type"></a>

This list is not relevant for Runtime Integrity

| Java                                                                                                                                | Go                                                                                                                                  | OS executables                                                                                                                      |
| ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------- |
| ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) | ![:check\_mark:](https://jfrog-int.atlassian.net/gateway/api/emoji/62d6e2d0-84c6-4564-9b2c-7379252a974d/atlassian-check\_mark/path) |

&#x20;
