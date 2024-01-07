Vagrant.configure("2") do |config|
  (1..3).each do |i|
    config.vm.define "node-#{i}.ansible.internal" do |node|
      node.vm.box = "generic/ubuntu2204"
      node.vm.hostname = "node-#{i}.ansible.internal"
      node.vm.network "private_network", ip: "192.168.50.2#{i}"

      node.vm.provider "virtualbox" do |vb|
          vb.memory =  "6144"
      end
    end
  end
end
