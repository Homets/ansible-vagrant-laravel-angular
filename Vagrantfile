# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "front" do |front|
    front.vm.hostname = "frontend"
    front.vm.box = "debian/buster64"
    front.vm.network :private_network, ip: "192.168.56.10"

  end

#  config.vm.define "back" do |back|
#    back.vm.hostname = "backend"
#    back.vm.box = "debian/buster64"
#    back.vm.network :private_network, ip: "10.0.0.102"
#  end

#  config.vm.define "db" do |db|
#    db.vm.hostname = "db"
#    db.vm.box = "debian/buster64"
#    db.vm.network :private_network, ip: "10.0.0.102"
#  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/configuration.yaml"
  end
end
