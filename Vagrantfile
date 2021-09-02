# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "smw" do |smw|
    smw.vm.box = "debian/buster64"
    # config.disksize.size = '30GB'
    smw.ssh.insert_key = false
    smw.vm.hostname = "smw.box"
    smw.vm.synced_folder ".", "/vagrant", create: true, disabled: false
    smw.vm.network :private_network, ip: "192.168.60.120"

    smw.vm.provider :virtualbox do |vb|
      vb.name = "smw_box"
      vb.memory = 4096
      vb.cpus = 2
    end
  end
  config.vm.provision "ansible_local" do |ansible|
    ansible.install = true
    ansible.version = "latest"
    ansible.compatibility_mode = "2.0"
    ansible.playbook = "ansible/playbook.yml"
    ansible.verbose = "true"
    ansible.extra_vars = { ansible_python_interpreter:"/usr/bin/python3" }
  end
end