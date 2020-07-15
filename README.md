# Bridges Parent POM
Install Bridges Parent POM to be able to build Docker images for automatic bridge installation (you will need a machine with Docker).

To install the POM, clone this repository and use

`mvn install`

Note: the docker daemon should be running on the same machine this pom will be installed or the installation process will fail.

### How to build bridge installation image
In the bridge repository:
* This POM file must be set as the bridge's parent POM.
* Bridge configuration file must be in /src/main/configuration
* Install and uninstall scripts must be in /src/main/script. Install script copies the bridge jar and any necessary dependencies that must be added to intermw (check the specific bridge guide for details).


To build a bridge and create the installation image, go to the bridge repository (local) and use:

`mvn clean package docker:build`
