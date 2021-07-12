Vagrant.configure("2") do |config|

    config.vm.define vm_name="nginx" do |node|
      node.vm.box = "vivien/nginx64"
      node.vm.hostname = vm_name
    end

    config.vm.provider "virtualbox" do |v|
      v.memory = 2048
      v.cpus = 2
    end
  end
