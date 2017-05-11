# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "fedora/25-cloud-base"

  config.vm.synced_folder ".", "/vagrant", type: "virtualbox"

  config.vm.provision "ansible" do |ansible|
    ansible.inventory_path = "ansible/vagrant-hosts"
    ansible.limit = "all"
    ansible.playbook = "ansible/site.yaml"
  end
end
