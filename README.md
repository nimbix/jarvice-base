# Overview
This is a collection of community-contributed JARVICE base images for developing high performance computing application on https://platform.jarvice.com using PushToCompute.

Contributed images are hosted on Docker Hub under the `jarvice/base-<image name>` namespace

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
