# Ansible

## Overview
This section covers Ansible, a powerful automation tool.

## Contents
- [Introduction](ansible/introduction.md)
- [Playbooks](ansible/playbooks.md)
- [Roles](ansible/roles.md)

## Docker Setup
To test Ansible scripts, you can use the following Docker setup.

### Dockerfile
Refer to the [Dockerfile](Dockerfile).

### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t ansible .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm ansible
    ```