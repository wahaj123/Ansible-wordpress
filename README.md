# Ansible-wordpress
### Ansible create vault
```
ansible-vault create path/to/folder/filename
then add the pass wp_pass: 1234
refer it in the playbook "{{wp_pass}}"
```
### Ansible deployment command
```
In order for multi-envirnoment the the host and group_var should exist in the same directory as in this project
```
### Ansible command
```
To deploy to specific enviroment
ansible-playbook playbook.yml -i inventory/prod  --ask-vault-password
```
### jenkins run ansible 
```
Plugins needed: Ansible, git
Clone the repo and then run the ansible command as in jenkins file
create the vault and ssh key that is need to ssh into the instance
```