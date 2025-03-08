## My Laravel Stack

This Ansible project, my_laravel_stack, automates the setup of a Laravel development or production environment on a target server. It provisions essential packages, configures a web server (Nginx), sets up PHP, installs Node.js via NVM, configures MariaDB as the database, and optionally sets up Zsh as the shell environment.

### Project Structure

```text
my_laravel_stack/
├── inventory/              # Inventory file(s) defining target hosts
├── playbook.yml            # Main playbook to orchestrate the roles
├── vars/                   # Variable files for customization
└── roles/
    ├── essential_packages/ # Installs base system packages
    ├── laravel_setup/     # Configures Laravel-specific setup
    ├── mariadb/           # Installs and configures MariaDB
    ├── nginx/             # Installs and configures Nginx web server
    ├── nvm_node/          # Installs Node.js via NVM
    ├── php/               # Installs and configures PHP
    └── zsh_setup/         # Sets up Zsh shell environment
```

- **inventory/**: Contains the list of target hosts where the stack will be deployed (e.g., hosts.yml or hosts.ini).
- **playbook.yml**: The main playbook that defines the order and application of roles.
- **vars/**: Directory for variable files (e.g., main.yml) to customize role behavior.
- **roles/**: Modular roles that handle specific tasks in the setup process.

### Prerequisites

Before running this Ansible project, ensure the following:

1. Ansible Installed: Install Ansible on your control machine (pip install ansible or via your package manager).
2. SSH Access: Ensure SSH access to the target hosts with a user that has sudo privileges.
3. Inventory Configuration: Update the inventory/ file with your target host details.
   Example inventory file (inventory/hosts.yml):

```yml
all:
  hosts:
    laravel_server:
      ansible_host: <your-server-ip>
      ansible_user: <your-ssh-user>
      ansible_ssh_private_key_file: ~/.ssh/id_rsa
```

### Roles

1. **essential_packages**
   Installs essential system packages (e.g., curl, git, unzip) required for the stack.
2. **laravel_setup**
   Configures a Laravel application, including cloning a repository, setting permissions, and running artisan commands (e.g., composer install, php artisan migrate).
3. **mariadb**
   Installs and configures MariaDB as the database server, creates a database, and sets up a user for Laravel.
4. **nginx**
   Installs Nginx and configures it as the web server to serve the Laravel application.
5. **nvm_node**
   Installs Node Version Manager (NVM) and a specified version of Node.js for Laravel frontend dependencies (e.g., npm for asset compilation).
6. **php**
   Installs PHP and required extensions (e.g., php-fpm, php-mysql) for Laravel.
7. **zsh_setup**
   Installs and configures Zsh as an optional shell environment for the server user.

### Variables

You can customize the behavior of roles by editing variable files in the vars/ directory or by passing extra variables during playbook execution. Example variables might include:

- PHP version (e.g., php_version: "8.3")
- Node.js version (e.g., node_version: "22")
- MariaDB database name and credentials
- Laravel application path (e.g., /var/www/laravel)

Example `vars/main.yml`

```yml
host_ip: ''
host_user: ''
laravel_db_name: ''
laravel_db_user: ''
```
