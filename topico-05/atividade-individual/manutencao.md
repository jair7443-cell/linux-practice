# Manutenção do Sistema

## Objetivo

Realizar verificações básicas de manutenção e validar o correto funcionamento do sistema Linux.

## Atividades Realizadas

### Monitorização do Sistema

Foram executados os seguintes comandos:

```bash
uptime
free -h
df -h
```

### Verificação de Utilizadores

```bash
who
```

### Consulta de Logs

```bash
journalctl -n 20
```

### Verificação do Serviço Crítico

```bash
systemctl status nginx
```

Resultado:
- Serviço ativo (running)
- Inicialização automática ativada (enabled)

## Conclusão

O sistema encontra-se funcional, com recursos disponíveis e o serviço Nginx operacional.
