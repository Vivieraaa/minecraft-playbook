# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu2204"

  config.ssh.insert_key = false

  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |v|
    v.linked_clone = true
  end

  # MC Server info
  config.vm.define "mcsv" do |mcsv|
    mcsv.vm.hostname = "orc-mcsv.test"
    mcsv.vm.network :private_network, ip: "192.168.42.4"
  end
end
