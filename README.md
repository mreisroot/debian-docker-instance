# Instância Vagrant do Debian com o Docker

Este é um Vagrantfile que, ao ser executado, cria uma máquina Debian (mas pode ser qualquer versão do Linux) e instala o Docker Engine ao chamar o script docker-setup.sh na linha de provisionamento do arquivo:

`config.vm.provision "shell", path: "docker-setup.sh"`

Tudo isso leva nada mais, nada menos que 2 MINUTOS e 41 SEGUNDOS para ser executado! :D

Obs: Essa duração ocorre quando já se tem a imagem Vagrant baixada na máquina local. Caso contrário, o Vagrant vai baixar a imagem, o que não é um processo demorado.

Para executar o Vagrantfile, execute no terminal:

`vagrant up`
