# Ansible Role: Takserver

This role installs the [TAK.gov](https://tak.gov/) takserver as a standalone single-server _mvp_.

## Setup

### Requirements

- Requires Ansible v2.15+

- Supports Debian and REHL-based Linux distributions.\
  See [galaxy_info](https://github.com/ThatKalle/ansible-role-takserver/blob/main/meta/main.yml#L10).

- Requires ansible galaxy collections to be installed:\
  See [requirements.yml](https://github.com/ThatKalle/ansible-role-takserver/blob/main/requirements.yml).

  ```bash
  ansible-galaxy collection install -r requirements.yml
  ```

## Example Playbook

```yml
- hosts: all
  become: true
  gather_facts: true

  roles:
    - takserver
```