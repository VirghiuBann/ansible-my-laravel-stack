# Role Name

This Ansible role configures a basic web server using Nginx.

## Requirements

- Ansible 2.18.2 or later
- Supported platforms:
  - Ubuntu 24.04.2 LTS

## Role Variables

### vars/main.yml

- domain_name: Custom domain name

## Dependencies

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

```yml
- hosts: webserver
  roles:
    - nginx
```

## License

MIT

## Author Information

Virghiu
