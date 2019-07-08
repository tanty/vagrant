# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "debian/buster64"

  # Disable automatic box update checking. If you disable this, then
  # boxes will only be checked for updates when the user runs
  # `vagrant box outdated`. This is not recommended.
  # config.vm.box_check_update = false

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # NOTE: This will enable public access to the opened port
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine and only allow access
  # via 127.0.0.1 to disable public access
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  # config.vm.synced_folder "../data", "/vagrant_data"

  # Provider-specific configuration so you can fine-tune various
  # backing providers for Vagrant. These expose provider-specific options.
  # Example for VirtualBox:

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    vb.gui = true

    # Customize the amount of memory on the VM:
    # vb.memory = "1024"
  end

  # View the documentation for the provider you are using for more
  # information on available options.

  # Enable provisioning with a shell script. Additional provisioners such as
  # Puppet, Chef, Ansible, Salt, and Docker are also available. Please see the
  # documentation for more information about their specific syntax and use.
  config.vm.provision "shell", inline: <<-SHELL
    apt update
    apt install -y xfce4 xfce4-xkb-plugin epiphany-browser weston
    sed 's:#autologin-user=:autologin-user=vagrant:' -i /etc/lightdm/lightdm.conf
    sudo -u vagrant -g vagrant rm -rf /home/vagrant/.config/xfce4
    sudo -u vagrant -g vagrant mkdir -p /home/vagrant/.config/xfce4
    sudo -u vagrant -g vagrant echo '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' | base64 -d | tar xJpf - -C /home/vagrant/.config/xfce4
    service lightdm restart
  SHELL
end
