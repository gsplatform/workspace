# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = "chef/centos-6.5"

  config.ssh.forward_agent = true

  # Automated deployment with Ansible
  config.vm.provision "ansible" do |ansible|

    ansible.playbook = "deployment/common-redhat/playbook.yml"
    ansible.inventory_path = "inventory/hosts.yml"

    ansible.sudo = true
    ansible.sudo_user = 'root'
    ansible.verbose = 'vvv'

    ansible.extra_vars = {
      ansible_ssh_user: 'vagrant'
    }
  end

  # Setup a development environment
  config.vm.define "dev" do |dev|

    dev.vm.network :forwarded_port, guest: 80,   host: 8000
    dev.vm.network :forwarded_port, guest: 8080, host: 8080
    dev.vm.network :forwarded_port, guest: 5000, host: 5000

    # Virtualbox configuration
    # (Adjust values to match your hardware)
    dev.vm.provider "virtualbox" do |vb|
      vb.cpus = 2
      vb.memory = 1024
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end

    # dev.vm.provision "shell", path: "inventory/dev/setup.sh"
    # dev.vm.provision "shell", path: "inventory/dev/data.sh"
  end

  # Setup a demo/production server
  config.vm.define "prod", autostart: false do |prod|
    # (TODO: configure a remote deployment)
  end

end
