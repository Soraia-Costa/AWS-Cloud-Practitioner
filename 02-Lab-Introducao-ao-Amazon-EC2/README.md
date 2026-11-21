# 11 – Lab: Introdução ao Amazon EC2

## Sobre o laboratório

Neste laboratório, explorei o serviço **Amazon EC2 (Elastic Compute Cloud)** da AWS, utilizado para criar e gerenciar servidores virtuais na nuvem.

O objetivo foi conhecer, na prática, o processo de criação, configuração, monitoramento e gerenciamento de uma instância EC2.

## Atividades realizadas

Durante o laboratório, desenvolvi as seguintes atividades:

- Criação de uma instância EC2 utilizando Amazon Linux 2023.
- Configuração das características da instância, incluindo tipo, armazenamento e rede.
- Configuração de um Security Group para controlar o acesso à instância.
- Configuração de um script User Data para instalação e inicialização do servidor web Apache.
- Verificação dos status checks e métricas de monitoramento da instância.
- Teste de acesso ao servidor web por meio do endereço IPv4 público.
- Liberação da porta 80 (HTTP) nas regras de entrada do Security Group.

## Resultado

Após configurar as regras de acesso, consegui acessar o servidor pelo navegador e visualizar a mensagem:

**Hello From Your Web Server!**

Essa atividade permitiu compreender melhor como uma instância EC2 pode hospedar uma aplicação web e como as configurações de rede e segurança influenciam sua disponibilidade.

## Principais aprendizados

- Conceitos básicos do Amazon EC2.
- Criação e configuração de servidores virtuais.
- Funcionamento dos Security Groups.
- Utilização de User Data para automatizar configurações.
- Monitoramento e verificação de integridade de instâncias.
- Acesso a aplicações hospedadas na AWS.

## Tecnologias e serviços utilizados

- Amazon EC2
- Amazon Linux 2023
- Security Groups
- Apache HTTP Server
- AWS Management Console

---

**Projeto desenvolvido durante meus estudos de Cloud Computing e preparação para a certificação AWS Certified Cloud Practitioner (CLF-C02).**
