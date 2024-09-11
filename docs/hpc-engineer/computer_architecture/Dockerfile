FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

COPY . /workspace
WORKDIR /workspace

CMD ["/bin/bash"]