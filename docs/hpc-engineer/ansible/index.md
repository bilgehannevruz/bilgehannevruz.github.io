# Ansible

## Overview
This section covers Ansible, a powerful automation tool.

## Contents
- [Introduction](ansible/introduction.md)
- [Playbooks](ansible/playbooks.md)
- [Roles](ansible/roles.md)

## Docker Setup
To test Ansible scripts, you can use the following Docker setup.

### Docker Compose Setup
We use Docker Compose to set up an Ansible controller and multiple nodes for testing.


### How to Build and Run
1. Build the Docker image:
    ```bash
    docker build -t ansible .
    ```

2. Run the Docker container:
    ```bash
    docker run -it --rm ansible
    ```

3. Use Docker Compose to set up the environment:
    ```bash
    docker-compose up -d
    ```

4. Access the Ansible controller:
    ```bash
    docker exec -it ansible-controller /bin/bash
    ```

5. Verify the setup by running an Ansible command:
    ```bash
    ansible all -m ping -i inventory
    ```

## Additional Resources
- [Ansible Documentation](https://docs.ansible.com)
- [Ansible GitHub Repository](https://github.com/ansible/ansible)