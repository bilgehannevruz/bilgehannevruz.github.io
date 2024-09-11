FROM ubuntu:20.04

RUN apt-get update && apt-get install -y \
    gcc \
    g++ \
    libomp-dev \
    openmpi-bin \
    openmpi-common \
    libopenmpi-dev \
    && rm -rf /var/lib/apt/lists/*

COPY . /workspace
WORKDIR /workspace

CMD ["/bin/bash"]