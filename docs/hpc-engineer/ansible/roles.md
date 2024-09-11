# Ansible Roles

## Overview
Ansible roles allow you to group related tasks, handlers, variables, and other Ansible components into reusable units. Roles help in organizing playbooks and making them more maintainable.

## Structure of a Role
A role has a specific directory structure. Here is an example:

### Example Role
Here is an example of a simple role that installs and starts Nginx.

#### `roles/nginx/tasks/main.yml`
```yaml
- name: Ensure Nginx is installed
  apt:
    name: nginx
    state: present

- name: Ensure Nginx is started
  service:
    name: nginx
    state: started
    enabled: yes
```

### Using Roles in a Playbook
To use a role in a playbook, you can include it in the roles section.

#### Example Playbook:
```yaml
- name: Apply common configuration
  hosts: all
  roles:
    - common

- name: Apply Nginx role
  hosts: webservers
  roles:
    - nginx
```


### Explanation
 - `roles`: A list of roles to apply to the hosts.

### Running a Playbook

To run a playbook, use the ansible-playbook command:
```bash
ansible-playbook -i inventory_file playbook_with_roles.yml
```




