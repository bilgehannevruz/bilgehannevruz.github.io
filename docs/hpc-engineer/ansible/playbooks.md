# Ansible Playbooks

## Overview
Ansible playbooks are YAML files that define a series of tasks to be executed on remote hosts. Playbooks are the core of Ansible's configuration, deployment, and orchestration capabilities.

## Structure of a Playbook
A playbook consists of one or more plays. Each play targets a group of hosts and defines tasks to be executed on those hosts.

### Example Playbook
Here is an example of a playbook that updates all packages on a group of servers.

```yaml
- name: Update all packages
  hosts: all
  become: yes
  tasks:
    - name: Update apt cache
      apt:
        update_cache: yes

    - name: Upgrade all packages
      apt:
        upgrade: dist
```


### Explanation
- `name`: A description of the play.
- `hosts`: The group of hosts to target.
- `become`: Whether to use privilege escalation (e.g., sudo).
- `tasks`: A list of tasks to execute.


### Running a Playbook
To run a playbook, use the ansible-playbook command:
```bash
ansible-playbook -i inventory_file playbook.yml
```


## Additional Resources
- [Ansible Playbooks Documentation](https://docs.ansible.com/ansible/latest/user_guide/playbooks.html)
