Vagrant.configure("2") do |config|
  config.vm.define "debian" do |debian|
    debian.vm.box = "debian/stretch64"
    debian.vm.network "public_network", bridge: "wlp2s0", ip: "192.168.100.117"
    debian.vm.provider "virtualbox" do |vb|
      vb.name = "debian_virtual_machine"
    end
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yml"    
  end
end