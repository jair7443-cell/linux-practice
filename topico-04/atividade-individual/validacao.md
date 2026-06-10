# Validação

## Serviço Web

### Comando utilizado

curl http://localhost

### Resultado

O serviço web respondeu corretamente, demonstrando que o Nginx se encontra em funcionamento.

## Firewall

### Comando utilizado

sudo ufw status

### Resultado

As regras configuradas para SSH e HTTP foram identificadas corretamente.

## Portas

### Comando utilizado

ss -tuln

### Resultado

Foram identificadas as portas necessárias para o funcionamento do servidor.

## Evidências

- Output do comando ss -tuln
- Output do comando sudo ufw status
- Output do comando curl http://localhost
- Output dos serviços em execução
