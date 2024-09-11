# GPU Computing

## Overview
This section covers GPU computing techniques and tools.

## Contents
- [Introduction](gpu_computing/introduction.md)
- [CUDA](gpu_computing/cuda.md)
- [OpenCL](gpu_computing/opencl.md)

## Docker Setup
To test GPU computing tools, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t gpu_computing .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm gpu_computing
    ```