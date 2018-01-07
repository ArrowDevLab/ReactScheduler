# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_check_update = false
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--vram", 16]
    vb.customize ["modifyvm", :id, "--memory", "2048"]
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    vb.gui = false
  end

  config.vbguest.auto_update = false
  config.vbguest.no_remote = true

  
  config.vm.network "public_network"
  config.vm.network "forwarded_port", guest: 3001, host: 3001
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provision "shell", :path => "provision_init.sh"
  config.vm.provision "shell", :path => "provision_base.sh",
    run: "always"
end
