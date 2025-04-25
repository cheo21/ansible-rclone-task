Vagrant.configure("2") do |config|
config.vm.box = "gusztavvargadr/windows-11"

config.vm.define "win1" do |win1|
    win1.vm.hostname = "win1"
    win1.vm.network "private_network", ip: "192.168.56.101"

    win1.vm.provider "virtualbox" do |vb|
      vb.name = "WindowsVM1"
      vb.memory = 3048
      vb.cpus = 2
    end
  end

 config.vm.define "win2" do |win2|
    win2.vm.hostname = "win2"
    win2.vm.network "private_network", ip: "192.168.56.102"

    win2.vm.provider "virtualbox" do |vb|
      vb.name = "WindowsVM2"
      vb.memory = 3048
      vb.cpus = 2
    end
  end
  
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/playbook.yml"
  end
end

