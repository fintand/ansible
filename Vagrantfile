# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "hashicorp/precise32"
  config.vm.box_check_update = false
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.synced_folder "./playbooks", "/playbooks"

  config.vm.provider "virtualbox" do |vb|  
    vb.memory = "1024"
  end

  config.vm.provision :shell, path: "bootstrap.sh"

end
