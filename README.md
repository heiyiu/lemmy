# Ansible Playbook for Deploying a Web Application

This repo contains an Ansible playbook that utilizes the lemmy ansible playbook to deploy a lemmy server with cloudflare ssl on a cloud instance.

## Requirements

- Ansible 2.9 or higher
- An Ubuntu server with SSH access and Python 3 installed
- A user account on the server with sudo privileges

## Usage

1. Run the preinstall playbook to set up the configuration files and cloudflare settings
```bash
ansible-playbook  --ask-vault-pass ansible/lemmy_preinstall.yml
```
2. Install the lemmy server
```bash
ansible-playbook --ask-become-pass --become -i lemmy-ansible/inventory/ lemmy_install.yml
```


