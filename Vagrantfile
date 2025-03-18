Vagrant.configure("2") do |config|

  config.vm.provision "file", source: "files/vagrant_practicum.pub", destination: "/home/vagrant/.ssh/"
  config.vm.define "practicum_server" do |practicum_server|
    practicum_server.vm.box = "centos9"
    practicum_server.vm.hostname = "practicum-server"
    practicum_server.vm.network "private_network", ip: "192.168.56.41"

    practicum_server.vm.provider "virtualbox" do |vb|
      vb.memory = 8192
      vb.cpus = 2 
    end

    practicum_server.vm.provision "shell", inline: <<-SHELL
      chmod 644 /home/vagrant/.ssh/vagrant_practicum.pub
      cat /home/vagrant/.ssh/vagrant_practicum.pub >> /home/vagrant/.ssh/authorized_keys
    SHELL
  end

end
