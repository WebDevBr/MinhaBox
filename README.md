# Box Desenvolvimento

Este box traz uma máquina virtual rodando Xbuntu 14.04 nas versões x86 ou x64 com os seguintes pacotes:

 - Nginx
 - PHP 5.6
 - Composer
 - Mysql 5.6
 - Adminer

## Instalar

Para instalar este box na versão x64 rode os comandos abaixo nesta exata ordem

	clone git@github.com:WebDevBr/MinhaBox.git MinhaBox
	cd MinhaBox
	vagrant up

Se quiser o box na versão x86 siga os passo abaixo.

Rode os comandos:

	clone git@github.com:WebDevBr/MinhaBox.git MinhaBox
	cd MinhaBox

Abra o arquivo `puphpnet/config.yaml` e nas linhas 4 e 5 substitua o final `-x64` por `-x32`, vai ficar assim:

	vagrantfile:
    target: local
    vm:
        box: puphpet/ubuntu1404-x32
        box_url: puphpet/ubuntu1404-x32

E para finalizar, rode `vagrant up` no terminal.

A primeira máquina virtual que você subir vai baixar a imagem do Ubuntu, portanto isso pode demorar um pouco mais, assim como a primeira vez que rodar qualquer box, já que ele vai baixar e instalar todos os pacotes, mas isso só a primeira vez, depois o processo é bem mais rápido.

## Acessar a máquina virtual

Para acessar a máquina virtual voê pode rodar o comando `vagrant ssh`, no caso do Windows ele irá te informar os dados para usar no [PuTTy](http://www.putty.org/).

## Requisitos

Para rodar esta máquina virtual você precisa:

 - [Vagrant >= 1.6.0](https://www.vagrantup.com/)
 - [Git](http://git-scm.com/)

Att. Erik