# Auto Deploy SSH Keys to Servers

This project uses Ansible to automatically deploy your public SSH key to a fleet of Linux servers.

##  Prerequisites
- Python 3 & Ansible installed
- SSH access to target servers
- A public SSH key

##  SSH Key
The public key is passed as an environment variable `PUBLIC_KEY` to avoid storing it in plaintext.

##  Usage

```bash
export PUBLIC_KEY="$(cat ~/.ssh/id_rsa.pub)"
ansible-playbook deploy-ssh-key.yml
