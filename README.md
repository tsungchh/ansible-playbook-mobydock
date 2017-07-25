# Ansible playbook for setup mobydock app

### Set up dev file and group_vars/all/unix_account_info
1. Setup host and user name in dev file
1. Setup unix_user, host_ip and pubkey_file in group_vars/all/unix_account_info

### Provision server
ansible-playbook provision.yml

### Setup postgres, redis, nginx and mobydock
ansible-playbook site.yml
