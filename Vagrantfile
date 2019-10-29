# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  
  ##VM1

  config.vm.box = "ubuntu/bionic64"

  config.vm.define "database" do |database|
    database.vm.box = "MiniDC-database"
    database.vm.hostname = "database"
    database.vm.network "private_network", ip: "172.17.177.21"

  ## Configurações de Size da VM
  config.vm.provider "virtualbox" do |v|
     v.name = "database"
     v.memory = 512
     v.cpus = 2
  end
end

  ##VM2
  
  config.vm.box = "ubuntu/bionic64"

  config.vm.define "blog" do |blog|
    blog.vm.box = "MiniDC-Blog"
    blog.vm.hostname = "Blog"
    blog.vm.network "private_network", ip: "172.17.177.22"

  ## Configurações de Size da VM
  config.vm.provider "virtualbox" do |v|
     v.name = "blog"
     v.memory = 512
     v.cpus = 2
  end
end

  ##VM3

  config.vm.box = "ubuntu/bionic64"

  config.vm.define "MiniDC-AnsibleController" do |controller|
    controller.vm.box = "MiniDC-controller"
    controller.vm.hostname = "controller"
    controller.vm.network "private_network", ip: "172.17.177.11"

  ## Configurações de Size da VM
  config.vm.provider "virtualbox" do |v|
     v.name = "controller"
     v.memory = 512
     v.cpus = 2
  end
end

end
  
