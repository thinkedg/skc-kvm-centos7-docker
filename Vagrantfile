# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define :cnt_docker do |cnt_config|
      cnt_config.vm.provider "libvirt"
      cnt_config.vm.box = "centos/7"
      cnt_config.vm.hostname = "cntdocker"
  end
  
  config.vm.provision "ansible" do |ansible|
      ansible.verbose = "v"
      ansible.playbook = "./provision/ansible/build.yml"
      ansible.config_file = "./provision/ansible/ansible.cfg"
  end
  
end
