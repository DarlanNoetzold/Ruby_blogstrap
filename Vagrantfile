# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "generic/debian10"
  config.ssh.forward_agent = true
  config.ssh.insert_key = false
  config.vm.box_download_insecure=true

  config.vm.network :forwarded_port, guest: 3000, host: 3000 # rails
  config.vm.network :forwarded_port, guest: 1080, host: 1080 # mailcatcher
  config.vm.network :forwarded_port, guest: 3306, host: 3306 # mysql
  config.vm.network :forwarded_port, guest: 5432, host: 5432 # postgresql
  config.vm.synced_folder "D:/Documentos/Projetos/RubyV2", "/home/vagrant"
end
