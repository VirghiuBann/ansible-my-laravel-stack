# Ansible Redis Role

=========

This Ansible role installs and configures Redis on an Ubuntu server. It is suitable for use with Laravel, caching, and queue services.

## Requirements

- Ansible 2.18.2 or higher
- Ubuntu 24.04 LTS

## Role Variables

This role includes the following configurable variables (you can override them via your own private Ansible vault or inventory):

### Default Variables

```yaml
redis_bind_address: '127.0.0.1' # Overwritten by private protected vars
redis_port: 6379 # Overwritten by private protected vars
redis_protected_mode: 'yes' # Overwritten by private protected vars
redis_appendonly: 'no' # Overwritten by private protected vars
redis_save: '' # Overwritten by private protected vars
```

## Dependencies

This role has no dependencies.

## Example Playbook

---

- hosts: all
  become: yes
  roles:
  - redis

## License

MIT
