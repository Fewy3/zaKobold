# This dockerfile is meant to serve as a rocm base image.  It registers the debian rocm package repository, and
# installs the rocm-dev package.

FROM mambaorg/micromamba
WORKDIR /content/
COPY env.yml /home/mambauser/env.yml
RUN micromamba install -y -n base -f /home/mambauser/env.yml
USER root
RUN apt update && apt install xorg aria2 -y
