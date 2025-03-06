# Laravel Setup Ansible Role

This Ansible role installs Composer, sets up the Laravel Installer globally, creates a new Laravel application using `laravel new example-app`, and manually installs `wkhtmltopdf` from a specific .deb package on an Ubuntu server. It assumes PHP and required extensions are already installed.

## Requirements

- **Ansible**: Version 2.18.2 or higher
- **Target System**: Ubuntu (all versions, tested with Jammy for wkhtmltopdf)
- **Pre-installed**: PHP and required extensions (e.g., mbstring, xml, zip)
- **Privileges**: Requires `become: true`

## Role Variables

```yaml
laravel_user: 'odin'
wkhtmltopdf_url: 'https://github.com/wkhtmltopdf/packaging/releases/download/0.12.6.1-2/wkhtmltox_0.12.6.1-2.jammy_amd64.deb' # wkhtmltopdf download URL
wkhtmltopdf_deb: '/tmp/wkhtmltox_0.12.6.1-2.jammy_amd64.deb' # Temporary .deb file location
```
