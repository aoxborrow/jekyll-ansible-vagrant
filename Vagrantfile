# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
Vagrant.require_version ">= 1.8.2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/ubuntu-14.04"
  config.vm.network :private_network, ip: "192.168.33.33"
  config.vm.synced_folder ".", "/vagrant", type: "nfs"
  config.ssh.insert_key = false
  config.ssh.forward_agent = true

  # install Ansible within the VM and run our playbook
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible/jav.yml"
  end

  config.vm.provider "vmware_fusion" do |vf|
    vf.gui = true
    vf.vmx['displayname'] = "jav"
    vf.vmx["memsize"] = "1024"
    vf.vmx["numvcpus"] = "2"
  end

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.name = "jav"
    vb.memory = "1024"
    vb.cpus = 2
  end
end
