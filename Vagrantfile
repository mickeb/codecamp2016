# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.define "kali" do |kali|
    kali.vm.box   = "mickeb/mejslakali"

    kali.vm.guest = :debian
    kali.vm.network "private_network", type: "dhcp"

    kali.vm.provider "virtualbox" do |vb|
      vb.gui = true

      vb.cpus   = 4
      vb.memory = "2048"
    end
  end

  config.vm.define "webgoat" do |webgoat|
    webgoat.vm.box = "mickeb/mejslawebgoat"

    webgoat.vm.network "private_network", type: "dhcp"

    # Enable WebGoat access from outside world
    # webgoat.vm.network "forwarded_port", guest: 8080, host: 8080

    webgoat.vm.provider "virtualbox" do |vb|
      vb.cpus   = 4
      vb.memory = "1024"
    end
  end
end
