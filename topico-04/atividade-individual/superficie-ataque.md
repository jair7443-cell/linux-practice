# Superfície de Ataque

## Serviço publicado

Servidor Web: Nginx

Sistema Operativo: Ubuntu Linux

Diretório de publicação:
/var/www/html/topico-03/

Porta utilizada:
80 (HTTP)

## Serviços identificados

- SSH
- Nginx
- Serviços internos do sistema

## Portas observadas

| Porta | Serviço | Necessária |
   22      SSH         Sim
   80     HTTP         Sim 
   443    HTTPS      Futuramente 

## Riscos identificados

- Tentativas de acesso indevido via SSH.
- Comunicação HTTP sem encriptação.
- Exposição de ficheiros sensíveis.
- Utilização de palavras-passe fracas.
- Serviços desnecessários ativos.

## Medidas iniciais

- Utilizar palavras-passe fortes.
- Rever permissões.
- Ativar firewall.
- Atualizar o sistema regularmente.
