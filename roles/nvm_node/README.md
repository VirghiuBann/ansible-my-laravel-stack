# NVM Node Ansible Role

This Ansible role installs Node Version Manager (NVM) and a specified version of Node.js for a user on Ubuntu-based systems. It ensures NVM is configured and Node.js is ready for use.

## Requirements

- **Ansible**: Version 2.18.2 or higher
- **Target System**: Ubuntu (all versions supported)
- **Privileges**: Tasks require `become: true` for package installation and user modification

## Role Variables

The role uses the following default variables, which can be overridden:

```yaml
# defaults/main.yml
nvm_user: 'odin' # The user to configure NVM and Node.js for
nvm_version: 'v0.40.1' # NVM version to install
node_version: '20.17.0' # Node.js version to install
nvm_install_url: 'https://raw.githubusercontent.com/nvm-sh/nvm/{{ nvm_version }}/install.sh'
```

## Dependencies

This role has no external dependencies but requires curl (installed by the role).

## Example Playbook

Install NVM and Node.js for the default user (odin):

```yml
---
- hosts: all
  become: true
  roles:
    - role: nvm_node
```

## License

MIT

## Author Information

virghiu
