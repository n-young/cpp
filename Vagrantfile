Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  config.ssh.forward_agent = true
  config.ssh.forward_x11 = true
  config.vm.provision "shell", inline: <<-SHELL
    rm -fv /etc/ssh/ssh_host_*
    dpkg-reconfigure openssh-server

    sudo apt-get -y update
    sudo apt-get -y install \
        build-essential \
        clang-8 \
        clang-format-8 \
        clang-tidy-8 \
        cmake \
        cscope \
        doxygen \
        gdb \
        git \
        g++-7 \
        make \
        pkg-config \
        valgrind \
        zlib1g-dev
  SHELL
end
