Vagrant.configure("2") do |config|
    
    config.vm.define "nexus" do |nexus|
        nexus.vm.box = "centos/7"
        nexus.vm.hostname = "nexus"
        nexus.vm.network "private_network", ip: "192.168.56.56"
        nexus.vm.provision "shell", path: "scripts/nexus-setup-centos.sh"
      end
  end
  

