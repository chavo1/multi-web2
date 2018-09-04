Vagrant.configure("2") do |config|
  
  (1..2).each do |i|
    config.vm.define vm_name="web0#{i}" do |node|
      node.vm.box = "chavo1/xenial"
      node.vm.network "private_network", ip: "192.168.56.5#{i}"
      node.vm.provision :shell, path: "scripts/provision.sh"
      node.vm.hostname = vm_name
    end
  end

  config.vm.define vm_name="mysql" do |node|
    node.vm.box = "chavo1/mysql"
    node.vm.network "private_network", ip: "192.168.56.58"
    node.vm.hostname = vm_name
  end
end
