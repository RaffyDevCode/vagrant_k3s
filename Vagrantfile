#Instalacja VM z k3s

Vagrant.configure("2") do |config|
    config.vm.define "vagrantk3s" do |vagrantk3s|
        vagrantk3s.vm.box_download_insecure = true
        vagrantk3s.vm.box = "generic/alpine319"
        vagrantk3s.vm.network "private_network", ip: "100.0.0.1"
        vagrantk3s.vm.hostname = "vagrantk3s"
        vagrantk3s.vm.provider "virtualbox" do |v|
        v.name = "vagrantk3s"
        v.memory = 3064
        v.cpus = 4
      config.vm.provision "shell", inline: <<-SHELL
          curl -sfL https://get.k3s.io | sh -
          while [ ! -f /etc/rancher/k3s/k3s.yaml ]; do sleep 1; done; sudo chmod 644 /etc/rancher/k3s/k3s.yaml;
      SHELL
      end
    end
end