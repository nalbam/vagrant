# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    # base box
    config.vm.box = "centos/6"

    # network adapter
    config.vm.network "private_network", ip: "192.168.33.10"

    # VM configure
    config.vm.provider "virtualbox" do |vb|
        vb.name = "yanolja"
        vb.customize ["modifyvm", :id, "--memory", 1024]
        vb.customize ["modifyvm", :id, "--cpus", 1]
    end

    # ssh
    config.ssh.forward_agent = true
    config.ssh.insert_key = false

    # shared folder
    config.vm.synced_folder "..", "/data"

    # install package
    #config.vm.provision "shell", path: "./bin/0.init.sh"
    #config.vm.provision "shell", path: "./bin/2.config.sh"
    #config.vm.provision "shell", path: "./bin/3.library.sh"
    #config.vm.provision "shell", path: "./bin/6.php55.sh"
    #config.vm.provision "shell", path: "./bin/8.composer.sh"
    #config.vm.provision "shell", path: "./bin/9.vhost.sh"
end
