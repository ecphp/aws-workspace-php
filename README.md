# Amazon Linux 2 WorkSpace - PHP development environment - Ansible playbook

## About

This Ansible playbook installs a working PHP development environment on
[Amazon Linux 2 WorkSpaces](https://aws.amazon.com/workspaces/).

It currently provides:

* PHP 7.2
* Git
* Apache 2.4
* MariaDB 10.2
* SQLite 3
* Composer
* PhpStorm (license not included)

## Usage

* If Ansible is not installed yet on the control machine, install it with:
  `sudo amazon-linux-extras install ansible2`
* If you want to install the environment on multiple workspaces, create a `hosts` file listing your [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html).
* If you want to install the environment on the local workspace only, you do not need to create a `hosts` file; simply replace `hosts` by `hosts.localhost` in the line below.
* Execute the playbook: `ansible-playbook -i hosts site.yml --ask-pass --ask-become-pass`.
* After execution of the playbook, you may need to log out then log in for the PhpStorm entry to appear in the Applications menu.
