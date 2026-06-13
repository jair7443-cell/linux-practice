# Monitorização do Sistema

## Tempo de Atividade

Comando utilizado:

```bash
uptime

#Resultado
13:31:26 up 22 min, 1 user, load average: 0,05, 0,02, 0,02

#Memória RAM
Comando utilizado:
free -h

#Resultado
Memória Total: 1,9 GiB
Utilizada: 701 MiB
Livre: 105 MiB
Cache: 1,3 GiB
Disponível: 1,2 GiB

Swap:
Total: 511 MiB
Utilizada: 0 B
Livre: 511 MiB

#Análise:
A utilização da memória encontra-se dentro dos parâmetros normais e não existe utilização da área de swap.

#Espaço em Disco
Comando utilizado:
df -h

#resultado Principal:
/dev/sda1
Tamanho: 25G
Utilizado: 9,9G
Livre: 14G
Utilização: 43%

#Análise:
O disco possui espaço suficiente para armazenamento e funcionamento do sistema.

#Utilizadores Ligados
Comando utilizado:

who

#Resultado:
jairmendes tty2 2026-06-13 13:09 (:0)

#Análise:
Existe um único utilizador autenticado no sistema.


