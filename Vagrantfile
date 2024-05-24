
Vagrant.configure("2") do |config|
  
  config.vm.box = "hashicorp/bionic64"
  config.vm.hostname = "devops-exam"

 
  config.vm.network "private_network", ip: "192.168.49.2"

 
  config.vm.provider "virtualbox" do |vb|
 
    vb.cpus = "2" 
    vb.memory = "4096"
    vb.name = "devops-vm"
   end
 
   config.vm.provision "shell", path: "setup.sh"

   config.vm.provision "shell" , inline: <<-SHELL
    sudo apt-get update && sudo apt upgrade -y
    sudo apt install git -y
   SHELL
end
