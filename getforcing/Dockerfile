# A docker container with pre-processing scripts installed as
# used in the eWaterCycle project for the forecast

# use ubuntua 18.04 as base
FROM ubuntu:18.04

LABEL maintainer=ewtrcycl
LABEL version=0.1

# update repositories
RUN apt-get -y update && \
apt-get -y upgrade

# Install dependencies
RUN apt-get -y install \
    sudo \
    wget \
    cdo

# set workdir
WORKDIR /usr/src

# copy scripts inside docker image
RUN mkdir -p /usr/src/scripts
COPY scripts /usr/src/scripts

# update PATH environment variable
ENV PATH=/usr/src/scripts:${PATH}

# command
CMD echo "test"
