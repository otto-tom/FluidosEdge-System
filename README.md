# Fluidos Edge System
This is a modified version of the [KubeEdge](https://github.com/kubeedge/kubeedge) repository designed to meet [Fluidos project](https://fluidos.eu) needs. It is a fork, or copy, of the official repository with changes made to align with the requirements of the project. The modifications will help to ensure that KubeEdge functions optimally within the Fluidos ecosystem. Additionally, these changes will enable the Fluidos team to contribute to the KubeEdge community by sharing their experiences with the modified version.

## Fluidos Edge architecture
![](docs/images/fluidos-edge-system.png)

## Features implementation phase

|                        | Fluidos Edge System v1.14 |
|------------------------|---------------------------|
| Router multicast       | OK                        |
| feature1               | Ongoing                   |
| feature2               | Rejected                  |
| featureN               | Pending review            |

## Build CloudCore
To build CloudCore, Docker runtime has to be installed. Instructions are available at the [official site](https://docs.docker.com/engine/install/) and also the [Fluidos Edge installation guide](https://github.com/otto-tom/Fluidos-Edge/tree/main/doc/installation-guide#edgecore--mqtt-broker). Also, "make" application is required, e.g., installing for a Debian based distribution:
```bash
sudo apt-get update
sudo apt-get install make -y
```

The following environmental variables should be considered:
- DOKERHUB_NS: your Docker Hub namespace (default: othontom) (optional)
- DOCKER_IMG_CTAG: custom tag for the generated image, e.g., *"-mytest"* (optional)

Start compilation and image build procedures using the following command:
```bash
make image WHAT=cloudcore -j8
```

## License

Fluidos Edge System is under the Apache 2.0 license. See the [LICENSE](LICENSE) file for details.
