## Overview
This section covers performance analysis techniques and tools.

## Contents
- [Introduction](performance_analysis/introduction.md)
- [Profiling](performance_analysis/profiling.md)
- [Benchmarking](performance_analysis/benchmarking.md)

## Docker Setup
To test performance analysis tools, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. **Build the Docker Image**:
    - Open a terminal and navigate to the directory containing the Dockerfile.
    - Run the following command to build the Docker image:
    ```bash
    docker build -t performance_analysis .
    ```

2. **Run the Docker Container**:
    - After building the image, run the following command to start the Docker container:
    ```bash
    docker run -it --rm performance_analysis
    ```

## Additional Resources
- [Gprof Documentation](https://sourceware.org/binutils/docs/gprof/)
- [Valgrind Documentation](http://valgrind.org/docs/manual/manual.html)