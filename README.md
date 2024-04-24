# vagrant_k3s

# Creating a VM (using the Vagrant provider) with Kubernetes installed - k3s.

* Required Vagrant: https://developer.hashicorp.com/vagrant/install

* Basic vagrant commands:  
  * `vagrant init` - initializing a new project in the current directory  
  * `vagrant up` - creating resources based on the Vagrantfile file  
  * `vagrant destroy -f` - deleting all resources  
  * `vagrant ssh hostname` - logging in via SSH to the created resource/VM

>[!NOTE]
Currently image based Vagrantfile: generic/alpine319

# Instruction

1. Install Vagrant: `https://developer.hashicorp.com/vagrant/install`
2. Clone repo: `gh repo clone RaffyDevCode/vagrant_k3s`
3. Issue a command in e.g. PowerShell: `vagrant up`
4. Logging in to the new machine: `vagrant ssh vagrantk3s`
5. Verification of a running cluster: `kubectl get all -n kube-system`
6. It's works!
