Vagrant.configure("2") do |config|

  # Configurando o SO e Rede
  config.vm.box = "debian/bullseye64"
  config.vm.network "public_network", bridge: "wlan0"

  # Configurando RAM, CPU e nome da máquina
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 1
    v.name = "debian-docker-instance"
  end

  # Provisionando a VM com o shell, executando um script que instala o Docker automaticamente
  config.vm.provision "shell", path: "docker-setup.sh"

end
