# ansible-cloudstack-ubuntu-aio
Ansible Playbook to install CloudStack All-in-one (aio) on Ubuntu 14.04 LTS (KVM, NFS Server, MySQL)

## Setup
Change ansible_hosts to your server IP or hostname.
Check and modify some variables in group_vars/env.yml

## Run with:
	ansible-playbook -s -i ansible_hosts -e host=<IP_hostname> -e user=<SSH_Username> cs-aio-deploy.yml

## Example:
	ansible-playbook -s -i ansible_hosts -e host=cs-aio1 -e user=ubuntu cs-aio-deploy.yml
