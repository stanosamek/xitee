Vagrant.configure("2") do |config|

# Define the xitee server machine
  config.vm.define "xitee" do |xitee|
    xitee.vm.box = "almalinux/9"
    xitee.vm.hostname = "wp"
    xitee.vm.network "private_network", ip: "192.168.122.2"

# Configuration of vm provider
    xitee.vm.provider "virtualbox" do |wp|
      wp.name = "wordpress"
      wp.memory = "2048"
      wp.cpus = 2
    end

# Copy SSH keys from the host to the guest machine
    xitee.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/id_rsa.pub" 
    xitee.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "~/.ssh/authorized_keys"

    xitee.vm.provision "shell", inline: <<-SHELL
      chown vagrant:vagrant /home/vagrant/.ssh/id_rsa.pub
      chmod 644 /home/vagrant/.ssh/id_rsa.pub
    SHELL
  end
  
end