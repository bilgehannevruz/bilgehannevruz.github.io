# Introduction to Ansible

## Overview
Ansible is an open-source automation tool used for configuration management, application deployment, and task automation. It uses a simple, human-readable language called YAML to describe automation jobs.

## Key Features
- **Agentless**: No need to install any software on the nodes.
- **Idempotent**: Ensures that the system reaches the desired state without unintended changes.
- **Extensible**: Supports custom modules and plugins.

## Example Playbook
Here is a simple example of an Ansible playbook that installs Nginx on a remote server.

```yaml
- name: Install Nginx
  hosts: webservers
  become: yes
  tasks:
    - name: Ensure Nginx is installed
      apt:
        name: nginx
        state: present
```

### How to Run
1. Create an inventory file hosts with the following content:
    ```yml
    [webservers]
    your_server_ip
    ```

2. Run the playbook
    ```bash
    ansible-playbook -i hosts install_nginx.yml
    ```