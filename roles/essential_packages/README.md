# Role Name

This Ansible role installs a set of essential packages on Debian/Ubuntu-based systems, specifically tailored for Ubuntu servers. It ensures that commonly used tools and utilities are available for system administration and development tasks.

## Requirements

Ansible: Version 2.18.2 or higher
Target System: Ubuntu (all versions supported)

## Role Variables

The role uses the following default variables, which can be overridden in your playbook or inventory:

```shell
# defaults/main.yml
essential_packages:
 - curl
 - git
 - htop
 - vim
 - unzip
 - zip

```

## Dependencies

This role has no external dependencies.

## Example Playbook

```shell
- hosts: all
  become: true  # Required to install packages
  roles:
    - role: essential_packages
```

## License

MIT

## Author Information

Virghiu
