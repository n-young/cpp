# Sample C++ Repository

This is a template repository to quickly set up a Vagrant virtual machine to write C or C++ code.

## Startup

First, install [Vagrant](https://www.vagrantup.com/).

Run `vagrant up` to start the vm, and `vagrant ssh` to access it. `vagrant halt` will stop the vm. `vagrant destroy` will delete all contents. `vagrant help` will display more help.

Everything in this directory will be synced to the vm in the `/vagrant` folder. It's recommended to add `cd /vagrant` to the last line of the `~/.profile` file.

## Installing Packages

This should be run on `vagrant up` automatically, but in case it isn't:

```bash
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
```
