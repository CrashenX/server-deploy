# server-deploy

Vagrant + Ansible to configure server

## Usage

### Requirements and setup

1. Ansible: http://docs.ansible.com/ansible/intro\_installation.html
   * Debian/Ubuntu: `sudo apt-get install ansible`

### Create your vault

Create a `group_vars/all/vault` from `group_vars/all/template.vault`
by replacing the bits in `<>` with your config values / secrets.

#### Encrypt your secrets

    ansible-vault encrypt group_vars/all/vault

### Setup your Server

    sudo ansible-playbook setup.yml --ask-vault-pass -i hosts

### Install Kubernetes with Snap, Conjure-up, and Juju

    https://kubernetes.io/docs/getting-started-guides/ubuntu/local/
