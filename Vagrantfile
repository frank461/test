Vagrant.configure(2) do |config|

  config.vm.define "web01" do |web01|
    web01.vm.box = "ubuntu/trusty64"
    web01.vm.hostname = "web01"
    web01.vm.network "private_network", ip: "10.1.1.11", netmask: "24"
    web01.vm.network "forwarded_port", guest: 80, host: 8084
    web01.vm.provision :shell, path: "bootstrap.sh"
  end
end