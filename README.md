# Overview
This is a collection of community-contributed JARVICE base images for developing high performance computing application on https://platform.jarvice.com using [PushToCompute](https://www.nimbix.net/pushtocompute-tutorial/).

Contributed images are hosted on [Docker Hub](https://hub.docker.com/u/jarvice) under the `jarvice/base-<image name>` namespace.

# Usage

Create a Dockerfile:

```bash
FROM jarvice/base-centos-mvapich2
MAINTAINER You

# Install your application
RUN /usr/local/install.sh
```

Test locally, for example:

```bash
docker build -t my-app .
docker run -p 443:443 -it my-app /usr/local/bin/nimbix_desktop /usr/local/entrypoint.sh
```

Use [PushToCompute](https://www.nimbix.net/pushtocompute-tutorial/) to deploy your high performance computing application on JARVICE.

# Contributing

## Updates and Bug Fixes
To contribute an update to a base image in this repository, please open an issue or pull request in the submodule's repository.

## Contributing images
To contribute a base image to the [JARVICE PushToCompute base images](https://hub.docker.com/u/jarvice), please open a pull request in this repository with details on the use case and testing criteria. If your pull request is accepted, we will fork your Dockerfile repository and manage all further coordination through our fork. Please follow the naming convention `base-<repository-name>` for contributed Dockerfile repositories.

Please include an example for using your contributed base image in the README.md, as well as documentation of intended use cases.


Welcome to JARVICE!

