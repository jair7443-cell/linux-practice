# Publicação do Site

## Nível escolhido
Nível 2 - Intermédio

## Rota escolhida
Nginx

## Ficheiros criados
- index.html
- sobre.html
- style.css

## Local de publicação
/var/www/html/topico-03/

## Comandos principais utilizados

```bash
sudo apt update
sudo apt install nginx -y

sudo systemctl start nginx
sudo systemctl enable nginx

sudo mkdir -p /var/www/html/topico-03

sudo cp ~/projeto_linux/topico-03/atividade-individual/site/* /var/www/html/topico-03/

curl http://localhost/topico-03

#Resultado obtido

-Foi criado e publicado um pequeno site web composto por duas páginas HTML e uma folha de estilos CSS. A publicação foi realizada com sucesso através do servidor web Nginx.

- O site ficou acessível localmente através do navegador, permitindo navegar entre as páginas e visualizar os estilos aplicados.
  Limitações encontradas

- Erro inicial na cópia dos ficheiros para o diretório de publicação.

- Necessidade de instalar e configurar o Nginx.

- Correção da codificação UTF-8 para apresentação correta dos caracteres acentuados.

- Ajustes na organização da estrutura de diretórios da atividade.
