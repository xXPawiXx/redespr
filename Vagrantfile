Vagrant.configure("2") do |config|
config.vm.define :cliente do |cliente|
cliente.vm.box = "bento/centos-7.9"
cliente.vm.network :private_network, ip: "192.168.50.2"
cliente.vm.hostname = "cliente"
end
config.vm.define :servidor do |servidor|
servidor.vm.box = "bento/centos-7.9"
servidor.vm.network :private_network, ip: "192.168.50.3"
servidor.vm.network :forwarded_port, guest: 80, host:4567
servidor.vm.network :forwarded_port, guest: 443, host:4568
servidor.vm.hostname = "servidor"
end
end