# Linux System Administration

## Overview
This section covers Linux system administration tasks and tools.

## Contents
- [Introduction](linux_system_administration/introduction.md)
- [User Management](linux_system_administration/user_management.md)
- [System Monitoring](linux_system_administration/system_monitoring.md)

## Docker Setup
To test Linux system administration tools, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t linux_system_administration .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm linux_system_administration
    ```