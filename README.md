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
* Create a `hosts` file listing your [inventory](https://docs.ansible.com/ansible/latest/user_guide/intro_inventory.html).
* Execute the playbook: `ansible-playbook -i hosts site.yml --ask-pass --ask-become-pass`.
* That's it.
