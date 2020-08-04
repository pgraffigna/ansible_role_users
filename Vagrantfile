# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  config.vm.define "test" do |test|
    test.vm.box = "geerlingguy/ubuntu2004"
    test.vm.network "private_network", ip: "192.168.60.10"
    test.vm.hostname = "test-machine"

    test.vm.provider :virtualbox do |vbox|
      vbox.name = "test-machine"
      vbox.memory = 512
    end
  end
end