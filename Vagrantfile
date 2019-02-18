# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"
  config.ssh.insert_key = false

  config.vm.provider :virtualbox do |v|
    v.name = "dk1"
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.hostname = "dk1"
  config.vm.network :private_network, ip: "192.168.1.13"

  config.vm.define :dk1 do |dk1|
  end

  # Ansible provisioner.
  config.vm.provision "ansible" do |ansible|
    ansible.compatibility_mode = "2.0"
    ansible.playbook = "playbook.yml"
    ansible.become = true
  end

end
