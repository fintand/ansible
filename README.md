Ansible + Vagrant
-----------------

### Install Vagrant
Use Vagrantfile 

```vagrant up```

```vagrant ssh```

### Create Key
* ```ssh-keygen -t rsa -b 4096 -C "whatever@mail.com"```
*  Empty passphrase
* Put public ssh key on Remote Server (Digitalocean droplet)
* Create droplet if needed, I created 3

### Install Ansible
* ```sudo apt-get update```
* ```sudo apt-get install software-properties-common```
* ```sudo apt-get install python-software-properties -y```
* ```sudo apt-add-repository ppa:ansible/ansible```
* ```sudo apt-get install -y ansible```

Backup hosts file
* ```sudo mv hosts hosts.bak```
* ```sudo vi hosts```
```
[web]
<IP>
<IP>
<IP>
```
### Running Ansible
* ```ansible all -m ping -u root```
* ```ansible all -m ping -u root --private-key=~/.ssh/id_ansible```

### Running Playbook
Run nginx.yml playbook
* ```ansible-playbook nginx.yml```
