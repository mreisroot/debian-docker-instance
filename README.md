# Instância Vagrant do Debian com o Docker

Este é um Vagrantfile que, ao ser executado, cria uma máquina Debian (mas pode ser qualquer versão do Linux) e instala o Docker Engine ao chamar o script docker-setup.sh na linha de provisionamento do arquivo:

`config.vm.provision "shell", path: "docker-setup.sh"`

Para executar o Vagrantfile, execute no terminal:

`vagrant up`
