BOX_IMAGE = "ubuntu/bionic64"
NODE_COUNT = 2

Vagrant.configure("2") do |config|
	config.vm.define "master" do |subconfig|
		subconfig.vm.box = BOX_IMAGE
		subconfig.vm.hostname = "master"
		subconfig.vm.network "public_network", bridge: "Intel(R) Dual Band Wireless-AC 8265"
		subconfig.vm.network "private_network", ip: "192.168.56.110", virtualbox_intnet: "VirtualBox Host-Only Ethernet Adapter"
end
  (1..NODE_COUNT).each do |i|
    	config.vm.define "node#{i}" do |subconfig|
		subconfig.vm.box = BOX_IMAGE
		subconfig.vm.hostname = "node#{i}"
		subconfig.vm.network "public_network", bridge: "Intel(R) Dual Band Wireless-AC 8265"
		subconfig.vm.network "private_network", ip: "192.168.56.#{i+3}", virtualbox_intnet: "VirtualBox Host-Only Ethernet Adapter"
    end
end

config.vm.provider "virtualbox" do |v|
  v.memory = 2048
  v.cpus = 2
end

# Install on all machines  
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update -y
  SHELL
end

