# Ansible Role: Takserver

This role installs the [TAK.gov](https://tak.gov/) takserver as a standalone single-server _mvp_.

## Setup

### Requirements

- Requires the `community.general` collection to be installed:

  ```bash
  ansible-galaxy collection install community.general
  ```

## Example Playbook

```yml
- hosts: all
  become: true
  gather_facts: true

  roles:
    - takserver
```