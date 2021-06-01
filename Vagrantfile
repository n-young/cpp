Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true
  config.vm.provision "shell", inline: <<-SHELL
    rm -fv /etc/ssh/ssh_host_*
    dpkg-reconfigure openssh-server

    apt-get update
    sudo apt-get install make build-essential gdb git cscope -y
  SHELL
end
