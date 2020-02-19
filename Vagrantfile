# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "private_network", ip: "192.168.10.100"
  config.vm.synced_folder "./node-sample-app", "/home/vagrant/node-sample-app",
    owner: 'vagrant',
    group: 'root',
    mount_options: ["dmode=444" , "fmode=444"]
end
