# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "debian/jessie64"
  config.vm.box_check_update = "true"
  config.vm.hostname = "mapbox-dev"
  config.vm.box_check_update = true
  config.vm.synced_folder ".", "/home/vagrant/mapbox"
  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true

  config.vm.provider "virtualbox" do |vb|
    vb.name = "mapbox"
    vb.gui = false
    vb.memory = "4096"
    vb.cpus = 2
  end

  config.vm.provision "shell", inline: <<-SHELL
     sudo apt-get -y update
     sudo apt-get -y install wget unzip lxde chromium
     wget https://mapbox.s3.amazonaws.com/mapbox-studio/mapbox-studio-linux-x64-v0.3.3.zip
     unzip mapbox-studio-linux-x64-v0.3.3.zip -d mapbox-studio-linux-x64-v0.3.3
     rm mapbox-studio-linux-x64-v0.3.3.zip
  SHELL
end
