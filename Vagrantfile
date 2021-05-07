
  # _____              ____              _______        _   
  # |  __ \            / __ \            |__   __|      | |  
  # | |  | | _____   _| |  | |_ __  ___     | | ___  ___| |_ 
  # | |  | |/ _ \ \ / / |  | | '_ \/ __|    | |/ _ \/ __| __|
  # | |__| |  __/\ V /| |__| | |_) \__ \    | |  __/\__ \ |_ 
  # |_____/ \___| \_/  \____/| .__/|___/    |_|\___||___/\__|
  #                          | |                             
  #                          |_|                             
 
##########################
# Vagrantfile
#########################

VAGRANTFILE_API_VERSION = "2"

##########################
# Common Configuration
##########################
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM configuration.
  config.vm.box = "ubuntu/bionic64"
  config.ssh.insert_key = false
  config.vm.synced_folder ".", "/vagrant", disabled: false
  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

##########################
# VM Configuration
#########################
# k8s Master Node. 
  config.vm.define "c1-master1" do |app|
    app.vm.hostname = "c1-master1"
    app.vm.network :private_network, ip: "192.168.60.4"
  end

# k8s Node 1. 
  config.vm.define "c1-node1" do |app|
    app.vm.hostname = "c1-node1"
    app.vm.network :private_network, ip: "192.168.60.5"
  end

# k8s Node 2. 
  config.vm.define "c1-node2" do |app|
    app.vm.hostname = "c1-node2"
    app.vm.network :private_network, ip: "192.168.60.6"
  end
end
