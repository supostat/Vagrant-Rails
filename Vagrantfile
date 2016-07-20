# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "gbarbieru/xenial"
  config.vm.hostname = "rails.dev"

  config.landrush.enabled = true
  config.landrush.host_ip_address = '192.168.33.10'
  config.landrush.tld = 'rails.dev'

  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.network "forwarded_port", guest: 5432, host: 5432

  config.vm.synced_folder "../../projects", "/vagrant_data"

  config.vm.provision :shell, path: "bootstrap.sh", privileged: false
end
