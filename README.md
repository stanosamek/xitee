# xitee homework

# Get started

## Prerequisities

* installed Ansible
* installed docker compose v2 module from ansible galaxy
* installed Vagrant
* installed Virtualbox

```All binaries were installed in latest version```

## Clone repository

* create directory where you want to store repository
* change the directory on your system, e.g. xitee
* clone repository ```git clone https://github.com/stanosamek/xitee.git```

## Setting up vagrant

* run command ```vagrant up```
* update vagrant ssh config file with command ```vagrant ssh-config > .vagrant/ssh-config```
* check in inventory/inventory.yml ip address of host (correct ip address of provisioned host you can find in .vagrant/ssh-config)

## Running the playbook

```ansible-playbook xitee_homework.yml -i ./inventory/inventory.yml --ask-vault-pass```

# Documentation

* password to the vault is **password**
* in ansible vault are stored keys and password for user


