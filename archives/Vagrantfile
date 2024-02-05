# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  numberSrv=1
  (1..numberSrv).each do |i|
   #j=i+154
   config.vm.define "server#{i}" do |server|
  	server.vm.box = "ubuntu/trusty64"
  	server.vm.hostname = "server#{i}"
  	server#{i}.vm.network "private_network", ip: "192.168.1.server#{i+154}", auto_config: "false"
        server.vm.provider "virtualbox" do |v|
     		v.name   = "server#{i}"
     		v.memory = "1024"
     		v.cpus = 1
        end # provider

        config.vm.provision "ansible" do |ansible|
              ansible.playbook ="provisioning/playbook.yml"
        end #provision
   end #define
  end #each
end # configure

