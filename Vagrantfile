# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "CentOS 6.5 x86_64"
  config.vm.box_url = "https://github.com/2creatives/vagrant-centos/releases/download/v6.5.3/centos65-x86_64-20140116.box"
  config.vm.network "forwarded_port", guest: 8111, host: 8111
  
  config.vm.network :private_network, ip: "192.168.101.21"
  config.ssh.forward_agent = "true"
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook/site.yml"
  end

end