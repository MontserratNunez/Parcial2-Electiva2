FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y ansible python3 iputils-ping docker.io && \
    apt-get clean

WORKDIR /ansible-lab
CMD ["sleep", "infinity"]