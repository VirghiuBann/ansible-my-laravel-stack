# Docker Ansible Role

This Ansible role installs Docker, configures the Docker group for a specified user.

## Requirements

- **Ansible**: Version 2.18.2 or higher
- **Target System**: Ubuntu (all versions supported)
- **Privileges**: Requires `become: true` for package installation, service management, and user/group modifications

## Role Variables

Default variables are defined in `defaults/main.yml`:

```yaml
docker_user: 'odin' # User to manage Docker and run
```
