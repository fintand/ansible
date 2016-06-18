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
* Installed via Vagrant shell provison 

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
