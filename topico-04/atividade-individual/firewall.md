# Configuração da Firewall

## Verificação inicial

Comando utilizado:

sudo ufw status

## Regras aplicadas

Permitir SSH:

sudo ufw allow 22/tcp

Permitir HTTP:

sudo ufw allow 80/tcp

HTTPS não foi ativado nesta fase.

## Ativação

sudo ufw enable

## Resultado

A firewall foi configurada permitindo apenas os serviços necessários para administração remota e acesso ao serviço web.

## Regras finais

| Serviço | Porta |
   SSH        22
   HTTP       80
  HTTPS  Não configurado 
