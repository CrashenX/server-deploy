# server-deploy

Vagrant + Ansible to configure server

## Usage

### Requirements and setup

1. Ansible: http://docs.ansible.com/ansible/intro\_installation.html
   * Debian/Ubuntu: `sudo apt-get install ansible`

### Create your vault

Create a `host_vars/default/vault` from `host_vars/default/template.vault`
by replacing the bits in `<>` with your config values / secrets.

#### Encrypt your secrets

    ansible-vault encrypt group_vars/all/vault

### Setup your Server

    sudo ansible-playbook setup.yml --ask-vault-pass -i hosts
