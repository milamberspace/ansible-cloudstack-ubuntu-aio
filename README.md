# ansible-cloudstack-ubuntu-aio
[Ansible](http://ansible.com) Playbook to install [Apache CloudStack](cloudstack.apache.org) 4.4 in an All-in-one (aio) setup on Ubuntu 14.04 LTS (KVM, NFS Server, MySQL).

## Roles:
    - common (install some utils, add cloudbr0 (reboot the machine), add ntp, sysstat)
    - enable-ssh-root (specially for the node)
    - nfs_server
    - nfs_client
    - mysql
    - cloudstack-node (+ KVM/Libvrit)
    - cloudstack-manager

## Setup
Change ansible_hosts to your server IP or hostname.

Check and modify some variables in group_vars/env.yml

## Run with:
	ansible-playbook -s -i ansible_hosts -e host=<IP_hostname> -e user=<SSH_Username> cs-aio-deploy.yml

## Example:
	ansible-playbook -s -i ansible_hosts -e host=cs-aio1 -e user=ubuntu cs-aio-deploy.yml

## Apache CloudStack UI

After a successful running of playbook, go to http://IP_hostname:8080/client to access at the Apache CloudStack UI.
