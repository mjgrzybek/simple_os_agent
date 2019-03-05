Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.vm.network "public_network", bridge: "wlp3s0", ip: "192.168.0.16"
  config.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "/home/vagrant/.ssh/me.pub"
  config.vm.provision "shell", inline: <<-SHELL
    cat /home/vagrant/.ssh/me.pub >> /home/vagrant/.ssh/authorized_keys
    useradd -m -s /bin/bash -U gtg -u 667
    cp -pr /home/vagrant/.ssh /home/gtg/
    chown -R gtg:gtg /home/gtg
  SHELL
end
