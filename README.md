# ansible-playbooks
Playbook I made to update GitHub Desktop and Discord.

## Install Ansible 
Install Ansible by pasting the commands below into your command line
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
This installs GitHub Desktop and Discord

### Updating only one program:
#### GitHub Desktop
```
sudo ansible-pull -U https://github.com/RyanHaniff/ansible-playbooks.git --tags github
```
#### Discord
```
sudo ansible-pull -U https://github.com/RyanHaniff/ansible-playbooks.git --tags discord
```

## Latest GitHub Desktop version
You can find the latest version [here](https://github.com/shiftkey/desktop/releases/).

Copy the link and replace the old URL with the new one the local.yml file.
```
    - name: Download GitHub
      become: yes
      get_url:
        url: NEW_LINK_HERE
        dest: /etc/packages/github.deb
        mode: 0755
      tags:
        - github
```

## Resources
https://opensource.com/article/18/3/manage-workstation-ansible
https://docs.ansible.com/archive/ansible/2.3/get_url_module.html
