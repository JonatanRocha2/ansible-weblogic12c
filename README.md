# Instalando um WebLogic Server com Ansible

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Features

- Integração com AD e LDAP
- Start/stop/status usando systemctl
- Configuração de logrotate
- Aplicação de pathes
- Disponível versão 12c 14.1.1.0.0

## Tech

Este projeto usa as tecnologias:

- [Weblogic] - Servidor de aplicação em Java desenvolvido pela Oracle.
- [Ansible] - Automação de todo o processo de configuração.
- [python] - Scripts escritos em python versáteis e reutilizáveis.
- [WLST] - ferramenta de linha de comando do weblogic

## Installation

Este playbook depende de um servidor com JDK instalado. As urls dos downloads deverão ser incluídos no arquivo vars/main.yml. Os instaladores podem ser achados nos serviços Oracle Support ou Oracle Delivery.

Instale a dependência e use os comandos abaixo para execução:

```sh
git clone <link-do-projeto>
cd ansible-weblogic12c
ansible -playbook -i hosts -u <user> -k -t <console|node> -b -e "ambiente=<DEV|HOM|PROD> wls_version=<> wls_domain_name=<> wls_password=<> ldap_password=<> tipo=<unico|distribuido>" main.yml
```

## Docker

Para executar em um container, poderá usar a infraestrutura em /docker.

```sh
cd ansible-weblogic12c/docker
docker compose build -d -t weblogic12c .
```

O comando acima criará um container com a imagem do CentOS 7 com as portas 22 e 7001 abertas.

## License

**Free Software, Hell Yeah!**
