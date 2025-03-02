# Role Name

This Ansible role installs, configures, and secures a MariaDB database server. It sets up the root user with a password, disables insecure defaults (e.g., anonymous users, remote root login), and allows the creation of application-specific databases and users with tailored privileges.

## Requirements

- Ansible 2.18.2 or later
- Supported platforms:
- Ubuntu 24.04.2 LTS

- Python Modules:
  - PyMySQL or mysqlclient (installed on the target host for Ansible’s MySQL modules).
  - Install via: pip install PyMySQL or apt/yum install python3-PyMySQL.

## Role Variables

laravel_db_name: ''
laravel_db_user: ''
laravel_db_host: ''

### encrypted

mariadb_root_password: ''
laravel_db_password: ''

## Dependencies

## Example Playbook

```yml
- hosts: webserver
  roles:
    - mariadb
```

## License

MIT

## Author Information

Virghiu
