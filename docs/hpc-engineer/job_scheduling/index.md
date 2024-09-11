## Overview
This section covers job scheduling algorithms and tools.

## Contents
- [Introduction](job_scheduling/introduction.md)
- [Batch Scheduling](job_scheduling/batch_scheduling.md)
- [Real-Time Scheduling](job_scheduling/real_time_scheduling.md)
- [Slurm](job_scheduling/slurm.md)

## Docker Setup
To test job scheduling tools, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t job_scheduling .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm job_scheduling
    ```

3. Use Docker Compose to set up the environment:
    ```bash
    docker-compose up -d
    ```

4. Access the Slurm controller:
    ```bash
    docker exec -it slurm-controller /bin/bash
    ```

## Additional Resources
- [Slurm Documentation](https://slurm.schedmd.com/documentation.html)