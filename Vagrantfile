Vagrant.configure("2") do |config|
 if Vagrant.has_plugin? "vagrant-vbguest"
 config.vbguest.no_install = true
 config.vbguest.auto_update = false
 config.vbguest.no_remote = true
 config.vm.synced_folder "C:/Users/Rafael/Documents/Prueba_Carpeta", "/home/vagrant/conexion"

 
 end
 config.vm.define :cliente do |cliente|
 cliente.vm.box = "rafael_antoniogomez/Rafael_Gomez"
config.vm.box_version = "0.0.1"
 cliente.vm.network :private_network, ip: "192.168.30.5"
 cliente.vm.hostname = "cliente"
 end
 config.vm.define :servidor do |servidor|
 servidor.vm.box = "rafael_antoniogomez/Rafael_Gomez"
config.vm.box_version = "0.0.1"
 servidor.vm.network :private_network, ip: "192.168.30.4"
 servidor.vm.hostname = "servidor"
 servidor.vm.network "forwarded_port", guest: 80, host: 5080
 end
end