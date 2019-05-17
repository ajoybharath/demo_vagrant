Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.provider "virtualbox" do |v|
    v.memory = 512
    v.cpus = 1
   config.vm.network “forwarded_port”, guest: 80, host: 8080
   config.vm.synced_folder “data”, “/vagrant_data”
   config.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y apache2
   SHELL
end
