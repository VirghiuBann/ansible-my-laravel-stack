# Role Name

This Ansible role installs `zsh` and `oh-my-zsh` for a specified user on Ubuntu-based systems. It sets `zsh` as the default shell and configures `oh-my-zsh` for an enhanced shell experience.

## Requirements

- **Ansible**: Version 2.18.2 or higher
- **Target System**: Ubuntu (all versions supported)
- **Privileges**: Tasks require `become: true` for package installation and user modification

## Role Variables

The role uses the following default variables, which can be overridden:

```yml
# defaults/main.yml
zsh_user: 'odin' # The user to configure zsh and oh-my-zsh for
oh_my_zsh_install_url: 'https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh'
```

## Dependencies

This role has no external dependencies.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
---
- hosts: all
  become: true
  roles:
    - role: zsh_setup
```

## License

MIT

## Author Information

virghiu
