# https://hub.docker.com/r/jupyterhub/k8s-singleuser-sample
# https://github.com/jupyterhub/zero-to-jupyterhub-k8s/blob/main/images/singleuser-sample/Dockerfile
FROM quay.io/jupyterhub/k8s-singleuser-sample:latest

USER root

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt-get update \
  && apt-get upgrade -y \
  && apt-get install -y --no-install-recommends \
      build-essential \
      htop \
      make \
      wget \
  && rm -rf /var/lib/apt/lists/*

USER ${NB_USER}
