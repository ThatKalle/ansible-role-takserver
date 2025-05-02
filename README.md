# Ansible Role: Takserver

This role installs the [TAK.gov](https://tak.gov/) takserver as a standalone single-server _mvp_.

## Setup

Download the setup and verification files from TAK.gov [product center](https://tak.gov/products/tak-server) and place them in the `files/` directory.

Set `takserver_deb_filename` and/or `takserver_rpm_filename`.

```
roles/takserver
├── files 
│   ├── deb_policy.pol
│   ├── takserver-public-gpg.key
│   ├── takserver_5.4-RELEASE17_all.deb
│   └── takserver-5.4-RELEASE17.noarch.rpm
```
```yml
takserver_deb_filename: takserver_5.4-RELEASE17_all.deb
takserver_rpm_filename: takserver-5.4-RELEASE17.noarch.rpm
```


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