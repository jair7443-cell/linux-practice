# Plano de Continuidade Operacional

## Objetivo

Garantir a continuidade do serviço web em caso de falha, perda de dados ou interrupção do sistema.

---

## Serviço Crítico

Serviço identificado:

- Nginx

Função:

- Servidor web responsável por disponibilizar páginas e aplicações aos utilizadores.

Verificação do estado:

```bash
systemctl status nginx
```

Resultado:

- Serviço ativo (running)
- Inicialização automática ativada (enabled)

---

## Ficheiros e Configurações Críticas

Principais elementos a proteger:

- /etc/nginx/
- /var/www/html/
- /etc/hosts
- Configurações do sistema
- Conteúdo do website

---

## Logs Importantes

Logs utilizados para análise e diagnóstico:

### Logs do sistema

```bash
journalctl -n 20
```

### Histórico de sessões

```bash
last
```

### Logs do Nginx

```bash
sudo journalctl -u nginx
```

---

## Estratégia de Backup

Periodicidade recomendada:

- Diário para ficheiros críticos
- Semanal para sistema completo

Elementos a incluir:

- Configurações do Nginx
- Diretórios do website
- Ficheiros de configuração do sistema

---

## Procedimento de Recuperação

1. Identificar a falha.
2. Selecionar o backup mais recente.
3. Restaurar os ficheiros.
4. Verificar permissões.
5. Reiniciar o serviço.

Exemplo:

```bash
sudo systemctl restart nginx
```

---

## Critérios de Validação

Após a recuperação devem ser confirmados:

- Serviço Nginx ativo
- Website acessível
- Ficheiros recuperados corretamente
- Logs sem erros críticos

Verificações:

```bash
systemctl status nginx
```

```bash
curl localhost
```

---

## Conclusão

A implementação de backups regulares, monitorização contínua e procedimentos de recuperação documentados permite reduzir o impacto de falhas e garantir a continuidade operacional do serviço.
