![vagrant-2.2.10](https://img.shields.io/badge/vagrant-2.2.10-blue?style=flat-square)

Vagrantfile - Avançado
========================

![Capa](virtualbox-plus-vagrant.png "Capa")

## Labóratorio de Vagrant Avançado

Um Vagrantfile um pouco mais eleaborado com várias máquinas, interligados em uma rede interna, com reserva de recuros, como CPU, memória, implementação de script em bash shell para configuração das máquinas em tempo de deployment entre outros.


Requisitos
------------

Usar em uma máquina com um pouco mais de recursos para suportar a quantidade de máquinas.


Dependências
------------

Instalação padrão do Vagrant.

Rodando o Ambiente
-------------------

Tenha certeza de star na pasta onde encontra o Vagrantfile 

    $ vagrant up

Entrando via SSH nos servers:

    $ vagrant ssh devops
      exit

    $ vagrant ssh compliance
      exit 

    $ vagrant ssh docker
      exit 

    $ vagrant ssh git
      exit 

    $ vagrant ssh log
      exit 

Verificando o status:

    $ vagrant status

    $ vagrant global-status

Desligando e removendo o ambiente:

    $ vagrant halt

    $ vagrant destroy


Informações do Autor
------------------

- Este projeto foi criado por Willdimark Ragazzi Ventura, DevOps Engineer. (<fininho.cetec@gmail.com>)
- Linkedin [Perfil](https://www.linkedin.com/in/willdymark-ragazzi-ventura-ccna-devnetsecops-membro-anppd%C2%AE-a4422617//).
