# ansible-playbooks
Playbook I made to update Github desktop and Discord.

## Install Ansible 
Install ansible by pasting the commands below into your command line
```
sudo apt-get install software-properties-common
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
sudo apt-get install ansible
```

## How to run from the command line
Once Ansible is installed you can run the following command
```
sudo ansible-pull -U https://github.com/RyanHaniff/ansible-playbooks.git
```
This installs GitHub and Discord

### Updating only one program:
#### Github desktop
```
sudo ansible-pull -U https://github.com/RyanHaniff/ansible-playbooks.git --tags github
```
#### Discord
```
sudo ansible-pull -U https://github.com/RyanHaniff/ansible-playbooks.git --tags discord
```
