FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    openjdk-11-jdk \
    && rm -rf /var/lib/apt/lists/*

COPY . /workspace
WORKDIR /workspace

CMD ["/bin/bash"]