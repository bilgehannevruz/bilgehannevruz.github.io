# Performance Analysis

## Overview
This section covers performance analysis techniques and tools.

## Contents
- [Introduction](performance_analysis/introduction.md)
- [Profiling](performance_analysis/profiling.md)
- [Benchmarking](performance_analysis/benchmarking.md)

## Docker Setup
To test performance analysis tools, you can use the following Docker setup.

### Dockerfile
Refer to the [parallel_programming/Dockerfile](../parallel_programming/Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t performance_analysis .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm performance_analysis
    ```