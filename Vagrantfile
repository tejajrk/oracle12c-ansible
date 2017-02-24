# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "boxcutter/centos73"
  # config.vm.box_download_ca_cert = "root_ca.crt"
  config.vm.box_check_update = false

  config.vm.network "private_network", ip: "192.168.56.13"
  config.vm.hostname = "oradb"

  config.hostmanager.enabled = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.manage_host = true
  config.hostmanager.manage_guest = true

  config.vbguest.auto_update = false

  config.ssh.insert_key = true
  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
    vb.cpus = 4
    vb.name = "oradb"
    vb.gui = false
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "oracle-db.yml"
    ansible.inventory_path = "./inventory/hosts"
    ansible.limit = 'all'
  end
end
