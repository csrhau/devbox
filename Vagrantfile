# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "debian/jessie64"
  config.vm.hostname = "devbox"
  config.ssh.forward_agent
  config.vm.provider :virtualbox do |vb|
    vb.cpus = 2
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/devbox.yml"
    ansible.sudo = true
  end
end
