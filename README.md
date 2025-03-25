
# Ansible Homework: 

## Description
This is my homework project 

## Prerequisites
Before running this playbook, you will need:
- Ansible 2.9+
- Python 3
## Installation 
Before runnig this playbook istall community.general collection
- ansible-galaxy collection install community.general

## Configuration
# Git Clone and Checkout Instructions
   - git clone https://github.com/HaifaLach/homework.git
   - git branch
   - git checkout master
     
## Playbook 1: Install LAMP Stack and Copy index.php
This playbook installs the LAMP stack (Linux, Apache, MySQL, PHP) on a remote server and copies the index.php file to remote host.
- Tasks:
  - Install Apache, MySQL, and PHP.
  - Start and enable the Apache and MySQL services.
  - Configure firewalld to allow HTTP
  - Copy a basic index.php file to /var/www/html/.

- Usage:
ansible-playbook  -i ../inventory --ask-vault-pass lamp_deploy.yml
## Playbook 2: Configure Users with RSA Key
This playbook is designed to configure users on the remote server and set up their SSH access using RSA key pairs.
- Tasks:
   - Create new users.
   - Set up RSA SSH key-based authentication for users.
   - Copy the public key to the remote server's authorized keys.
- Usage:
ansible-playbook  -i ../inventory --ask-vault-pass users_csv.yml
## Playbook 3: Modify Host File Using Jinja2
This playbook modifies the /etc/hosts file on the remote machine using Jinja2 templates.
- Tasks:
  - Modify the /etc/hosts file based on a Jinja2 template.
  - Ensure correct host mappings are added to the file.
- Usage:
ansible-playbook modify-hosts-file.yml
