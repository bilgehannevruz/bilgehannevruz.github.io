# Distributed Systems

## Overview
This section covers the principles of distributed systems.

## Contents
- [Introduction](distributed_systems/introduction.md)
- [Consistency Models](distributed_systems/consistency_models.md)
- [Distributed Algorithms](distributed_systems/distributed_algorithms.md)

## Docker Setup
To test distributed systems tools, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t distributed_systems .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm distributed_systems
    ```