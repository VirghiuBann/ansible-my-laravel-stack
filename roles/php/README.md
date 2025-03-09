# Role Name

This Ansible role installs a specified version of PHP along with a set of commonly used PHP modules on Debian-based systems (e.g., Ubuntu, Debian). It uses the apt package manager to ensure PHP and its extensions are installed, making it ideal for setting up web application environments or development servers.

Key features:

Installs a configurable PHP version (e.g., 7.4, 8.1, 8.2).
Includes essential PHP modules like fpm, mysql, gd, curl, and more.
Ensures idempotency and supports dry-run testing with --check.

## Requirements

Ansible: Version 2.9 or higher.
Target System: Debian-based OS (Ubuntu or Debian) with apt package manager.
Privileges: Tasks require become: yes (sudo) to install packages.
PHP Repository: A repository supporting the desired PHP version (e.g., ppa:ondrej/php for Ubuntu) must be available or configured separately.

## Role Variables

Variables are defined in defaults/main.yml:

## |Variable| Description| Default Value| Example|

|{{php_version}} |The PHP version to install| "8.1"| "7.4", "8.2"|

## Dependencies

None. This role is self-contained.

## Example Playbook

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - php

## License

MIT

## Author Information

virghiu
