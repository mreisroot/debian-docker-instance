Vagrant.configure("2") do |config|

  # Cluster de VMs para trabalhar com Docker Swarm
#   (1..3).each do |i|
# 
#     config.vm.define "docker_#{i}" do |dock|
# 
#       # Definindo provider, nome no VirtualBox e alocando recursos
#       dock.vm.provider "virtualbox" do |v|
#         v.name = "docker_#{i}"
#         v.cpus = 1
#         v.memory = 768
#         v.gui = false
#       end
# 
#       # Definindo SO, hostnames e rede do Cluster
#       dock.vm.box = "debian/bullseye64"
#       dock.vm.hostname = "docker-#{i}"
#       dock.vm.network "private_network", ip: "192.168.56.1#{i}"
# 
#       # Provisionamento das VMs
#       dock.vm.provision "shell", path: "docker-setup.sh"
#       
#     end
# 
#   end

  # Uma única VM para trabalhar com Docker

  # Configurando o SO, hostname e Rede
  config.vm.box = "debian/bullseye64"
  config.vm.hostname = "docker"
  config.vm.network "private_network", ip: "192.168.56.11"

  # Configurando RAM, CPU e nome da máquina
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 1
    v.name = "debian_docker_instance"
  end

  # Provisionando a VM com o shell, executando um script que instala o Docker automaticamente
  config.vm.provision "shell", path: "docker-setup.sh"

end
