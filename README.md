# Amazon Linux 2 WorkSpace - PHP development environment - Ansible playbook

## About

This Ansible playbook installs a working PHP development environment on
[Amazon Linux 2 WorkSpaces](https://aws.amazon.com/workspaces/).

It currently provides:

* PHP 5.4 to 7.3 NTS (default: 7.2) and PHP-FPM
* Git
* Apache 2.4
* MariaDB 5.5
* SQLite 3
* Composer
* PhpStorm (license not included)
* Docker 18.06.1-ce and Docker Compose 1.24.0

PHP packages are provided by [Remi's RPM repository](https://rpms.remirepo.net/).

## Usage

* Create a `hosts` file listing your [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html).
* Update the `php_version` and `php_fpm_port` values in `roles/common/defaults/main.yml` according to your needs.
* Execute the playbook: `ansible-playbook -i hosts site.yml --ask-become-pass`.
* That's it.
