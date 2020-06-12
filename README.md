# Amazon Linux 2 WorkSpace - PHP development environment - Ansible playbook

## About

This Ansible playbook installs a working PHP development environment on
[Amazon Linux 2 WorkSpaces](https://aws.amazon.com/workspaces/).

It currently provides:

* PHP 5.4 to 7.4 NTS (default: 7.4) and PHP-FPM
* PHP OCI8 extension and Oracle Instant Client
* Git
* Apache 2.4
* MariaDB 5.5
* SQLite 3
* Composer
* PhpStorm (license not included)
* Docker and Docker Compose

PHP packages are provided by [Remi's RPM repository](https://rpms.remirepo.net/).

## Usage

* If Ansible is not installed yet on the control machine, install it with:
  `sudo amazon-linux-extras install ansible2`
* Update the `php_version` and `php_fpm_port` values in `roles/common/defaults/main.yml` according to your needs.
* If you want to install the environment on multiple workspaces, create a `hosts` file listing your [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html).
* If you want to install the environment on the local workspace only, you do not need to create a `hosts` file; simply replace `hosts` by `hosts.localhost` in the line below.
* Execute the playbook: `ansible-playbook -i hosts site.yml --ask-pass --ask-become-pass`.
* After execution of the playbook, you may need to log out then log in for the PhpStorm entry to appear in the Applications menu.
