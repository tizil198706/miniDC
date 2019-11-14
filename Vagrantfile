# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

    config.vm.define "db1" do |db|
    db.vm.box = "ubuntu/bionic64"
    db.vm.hostname = "MiniDc-Database1"
    db.vm.network "private_network", ip: "172.17.177.21"
     
    db.vm.provider "virtualbox" do |v|
     v.name = "MiniDC-DataBase1"
     v.memory = 512
     v.cpus = 1


    end
  end

  config.vm.define "blog1" do |blog|
    blog.vm.box = "ubuntu/bionic64"
    blog.vm.hostname = "MiniDC-Blog1"
    blog.vm.network "private_network", ip: "172.17.177.22"
  
    blog.vm.provider "virtualbox" do |v|
     v.name = "MiniDC-Blog1"
     v.memory = 512
     v.cpus = 1
    end
  end

  config.vm.define "controller1" do |controller|
    controller.vm.box = "ubuntu/bionic64"
    controller.vm.hostname = "MiniDC-AnsibleController1"
    controller.vm.network "private_network", ip: "172.17.177.11"
  
    controller.vm.provider "virtualbox" do |v|
     v.name = "MiniDC-AnsibleController1"
     v.memory = 512
     v.cpus = 1
    end
  end
end