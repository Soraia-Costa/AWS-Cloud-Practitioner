# Projeto 01 — Criação de VPC e Servidor Web na AWS

## Sobre o projeto

Este projeto foi desenvolvido durante uma atividade prática do AWS Academy / AWS re/Start, com o objetivo de criar uma infraestrutura de rede na AWS e disponibilizar um servidor web utilizando uma instância EC2.

Durante o laboratório, pratiquei a criação e configuração de uma VPC, sub-redes, tabelas de rotas, grupo de segurança e instância EC2.

## Serviços e tecnologias utilizados

- Amazon VPC
- Amazon EC2
- Security Groups
- Subnets (sub-redes públicas e privadas)
- Route Tables (tabelas de rotas)
- Amazon Linux 2
- Apache
- PHP
- AWS Academy

## Etapas realizadas

### 1. Criação da VPC

Criação de uma VPC com o nome `Lab VPC`.

- Bloco CIDR IPv4: `10.0.0.0/16`
- IPv6: não utilizado
- DNS habilitado

### 2. Criação das sub-redes

Foram criadas quatro sub-redes:

| Sub-rede | Bloco CIDR | Tipo |
|---|---|---|
| Public Subnet 1 | 10.0.0.0/20 | Pública |
| Private Subnet 1 | 10.0.128.0/20 | Privada |
| Public Subnet 2 | 10.0.16.0/24 | Pública |
| Private Subnet 2 | 10.0.144.0/24 | Privada |

### 3. Configuração das tabelas de rotas

Foram realizadas as associações:

- Public Subnet 1 e Public Subnet 2 → Public Route Table.
- Private Subnet 1 e Private Subnet 2 → Private Route Table.

### 4. Configuração do grupo de segurança

Criação do grupo `Web Security Group`.

Regra de entrada configurada:

- Tipo: HTTP
- Protocolo: TCP
- Porta: 80
- Origem: 0.0.0.0/0
- Descrição: Permit web requests.

### 5. Criação da instância EC2

Criação da instância com as seguintes configurações:

- Nome: Web Server 1
- AMI: Amazon Linux 2
- Tipo: t3.micro
- Par de chaves: vockey
- VPC: Lab VPC
- Sub-rede: Public Subnet 1
- IP público automático: habilitado
- Grupo de segurança: Web Security Group

### 6. Configuração do servidor web

Utilização do campo User Data para executar automaticamente um script de instalação e configuração.

O script realizou as seguintes tarefas:

- Instalação do Apache, MySQL e PHP.
- Download dos arquivos da aplicação.
- Extração dos arquivos para o diretório `/var/www/html/`.
- Configuração e inicialização do Apache.

## Resultado obtido

A instância EC2 foi iniciada com sucesso e apresentou três verificações de status aprovadas.

O servidor web foi acessado pelo navegador utilizando seu DNS público.

A página apresentou informações da instância, zona de disponibilidade e utilização de CPU, confirmando que o servidor estava respondendo às requisições HTTP.

## Conhecimentos praticados

- Criação e configuração de redes na AWS.
- Organização de sub-redes públicas e privadas.
- Associação de sub-redes a tabelas de rotas.
- Configuração de regras de segurança.
- Provisionamento de uma máquina virtual com EC2.
- Automação de configurações utilizando User Data.
- Instalação e inicialização de um servidor web Apache.
- Teste de acesso a uma aplicação por DNS público.

## Conclusão

Este laboratório proporcionou uma experiência prática com serviços fundamentais da AWS, permitindo compreender melhor como os componentes de rede e computação em nuvem trabalham em conjunto para disponibilizar um servidor web.

A atividade foi realizada em ambiente de laboratório AWS Academy, com finalidade educacional.
