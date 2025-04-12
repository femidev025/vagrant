# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # Define the first server
    config.vm.define "server1" do |server1|
      server1.vm.box = "ubuntu/jammy64"
      server1.vm.hostname = "server1"
      server1.vm.network "private_network", ip: "192.168.56.10"
      server1.vm.provider "virtualbox" do |vb|
        vb.memory = "1024" # 1GB RAM
        vb.cpus = 1
      end

      server1.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y net-tools vim
        echo "Server1 is ready!" > /home/vagrant/welcome.txt
      SHELL
    end
  
    # Define the second server
    config.vm.define "server2" do |server2|
      server2.vm.box = "ubuntu/jammy64"
      server2.vm.hostname = "server2"
      server2.vm.network "private_network", ip: "192.168.56.11"
      server2.vm.provider "virtualbox" do |vb|
        vb.memory = "1024" # 1GB RAM
        vb.cpus = 1
      end

      server2.vm.provision "shell", inline: <<-SHELL
        apt-get update
        apt-get install -y net-tools vim
        echo "Server2 is ready!" > /home/vagrant/welcome.txt
      SHELL
    end
  end