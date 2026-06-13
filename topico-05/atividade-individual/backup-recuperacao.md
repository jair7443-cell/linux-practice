# Backup e Recuperação Simples

## Objetivo

O objetivo desta atividade foi identificar um ficheiro crítico do sistema Linux, criar uma cópia de segurança (backup), realizar um teste de recuperação e validar a integridade dos dados restaurados.

---

## Identificação do Ficheiro Crítico

Foi selecionado o ficheiro:

```bash
/etc/hosts
```

Este ficheiro é utilizado pelo sistema operativo para associar nomes de máquinas a endereços IP locais, sendo importante para a resolução de nomes e funcionamento correto da rede.

---

## Criação do Backup

Primeiramente foi criada uma pasta para armazenar os ficheiros de backup:

```bash
mkdir backups

Em seguida foi copiado o ficheiro crítico para a pasta de backup:

```bash
cp /etc/hosts backups/
```

Posteriormente foi criada uma cópia de segurança comprimida utilizando o comando tar:

```bash
tar -czvf backups-hosts.tar.gz backups/
```

Resultado obtido:

* Backup criado com sucesso.
* Ficheiro gerado: `backups-hosts.tar.gz`.

---

## Teste de Recuperação

Para validar o backup foi criada uma pasta destinada aos testes de recuperação:

```bash
mkdir recuperacao-testes
```

O ficheiro de backup foi restaurado utilizando o comando:

```bash
tar -xzvf backups-hosts.tar.gz -C recuperacao-testes
```

Resultado obtido:

```text
backups/
backups/hosts
```

---

## Validação da Recuperação

Foi verificada a estrutura recuperada:

```bash
ls recuperacao-testes
```

Resultado:

```text
backups
```

Posteriormente foi validado o conteúdo do ficheiro restaurado:

```bash
cat recuperacao-testes/backups/hosts
```

Resultado:

```text
# Standard host addresses
127.0.0.1 localhost
::1 localhost ip6-localhost ip6-loopback
ff02::1 ip6-allnodes
ff02::2 ip6-allrouters
127.0.1.1 linuxPratica
```

A comparação confirmou que os dados foram restaurados corretamente.

---

## Importância dos Backups

A realização de cópias de segurança é uma prática fundamental para garantir a continuidade dos serviços e a proteção da informação. Os backups permitem recuperar ficheiros em situações como:

* Eliminação acidental de dados;
* Falhas de hardware;
* Corrupção de ficheiros;
* Ataques informáticos;
* Erros de configuração.

---

## Conclusão

A atividade foi concluída com sucesso. Foi possível criar uma cópia de segurança do ficheiro crítico `/etc/hosts`, restaurar os dados para uma localização de teste e validar a integridade do conteúdo recuperado.

O procedimento demonstrou a importância dos backups na administração de sistemas Linux e na implementação de estratégias de recuperação de desastres.
