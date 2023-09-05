Vagrant.configure("2") do |config|
    
    config.vm.define "nexus" do |nexus|
        nexus.vm.box = "centos/7"
        nexus.vm.hostname = "nexus"
        nexus.vm.network "private_network", ip: "192.168.56.56"
        nexus.vm.provision "shell", path: "scripts/nexus-setup-centos.sh"
    end

    config.vm.define "sonarqube" do |sonarqube|
        sonarqube.vm.box = "ubuntu/bionic64"
        sonarqube.vm.hostname = "sonarqube"
        sonarqube.vm.network "private_network", ip: "192.168.56.57"
        sonarqube.vm.provision "shell", path: "scripts/sonarqube-setup-ubuntu.sh"

        config.vm.provider "virtualbox" do |vb|
            vb.memory = 2048
            vb.cpus = 2
        end
    end

      
end
  

