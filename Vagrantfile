# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure('2') do |config|
  config.vm.box      = 'ubuntu/wily64'
  config.vm.hostname = 'vagrant-golang-box'

  # fix DNS issue
  # http://serverfault.com/a/506206
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end

  config.vm.network :forwarded_port, guest: 3000, host: 3000

  # PostgreSQL
  config.vm.network :forwarded_port, guest: 5432, host: 5433

  config.vm.provision :shell, path: 'vagrant-bootstrap.sh', keep_color: true

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end
end
