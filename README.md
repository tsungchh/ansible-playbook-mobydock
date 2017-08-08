# Ansible playbook for setup mobydock app

### Set up dev file and group_vars/all/unix_account_info
1. Setup host and user name in dev file
1. Setup unix_user, host_ip and pubkey_file in group_vars/all/unix_account_info

### Provision server
ansible-playbook provision.yml

### Setup postgres, redis, nginx and mobydock
ansible-playbook site.yml

### For first time setup postgres docker
1. Go into docker with "sudo docker exec -it postgres bash"
1. Switch to postgres user with "su postgres"
1. Enter postgres shell with "psql"
1. Create mobydock database "CREATE DATABASE mobydock;"
1. Create user "CREATE USER mobydock WITH PASSWORD 'yourpassword'; GRANT ALL PRIVILEGES ON DATABASE mobydock to mobydock;"
