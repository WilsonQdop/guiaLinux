---
author: Wilson Francisco, João Pedro, Isllâne
---
```
Colaboradores - Isllâne Maria, João Pedro, Wilson Francisco
```

- [1. Guia de comandos Linux](#1-guia-de-comandos-linux)
  - [1.1. Comandos](#11-comandos)
    - [1.1.1. - Obter informações do sistema](#111---obter-informações-do-sistema)
    - [1.1.2 - Navegação e manipulação de arquivos](#112---navegação-e-manipulação-de-arquivos)
    - [1.1.3 - Permições e controle de usuários](#113---permições-e-controle-de-usuários)
    - [1.1.4 - Gerenciamento de pacotes e serviço](#114---gerenciamento-de-pacotes-e-serviço)
    - [1.1.5 - Terminal](#115---terminal)
    - [1.1.6 - Rede](#116---rede)
    - [1.1.7 - Logs e monitoramento](#117---logs-e-monitoramento)
    - [1.1.8 - Deploy e backup](#118---deploy-e-backup)
  - [1.2. Atalhos do `terminal`](#12-atalhos-do-terminal)
  - [1.3 Editor de texto `(nano)`](#13-editor-de-texto-nano)
# 1. Guia de comandos Linux

Este README serve como um passo a passo ou guia de comandos simples que podemos usar no terminal do Linux. Com o intuito para estudos da disciplina de DevOps.

Poderá colocar print de tela, imagens... use a criatividade. (Editar)

## 1.1. Comandos

### 1.1.1. - Obter informações do sistema

| COMANDO     | O QUE FAZ | EXEMPLO |
| ----------- | --------- | ------- |
| **fastfetch** | Exibe informações do sistema de forma visualmente atraente. | `fastfetch` |
| **whoami**    | Mostra qual usuário está logado atualmente no sistema.      | `whoami` |
| **uptime** | Exibe informaçoes sobre o tempo de funcionamento do sistema. | `uptime` |
| **df** | Exibe informações ssobre o uso de espaço em disco em partições montadas. | `df -h` |
| **du -h** | Espaço usado por arquivos. |	`du -h arquivo` |
| **uname -a** | Infos do kernel. | `uname -a` |

### 1.1.2 - Navegação e manipulação de arquivos

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
| **cd**    | Muda de diretório. | `cd /home/usuario` |
| **pwd**   | Exibe em qual diretório você está. | `pwd`|
| **ls**    | Lista arquivos e diretórios. | `ls -alh` |
| **cat** | Exibe o conteúdo de arquivos na tela, junta o conteúdo de múltiplos arquivos em um só, cria novos arquivos e anexa texto a arquivos existentes. | `cat /etc/hosts` |
| **rmdir** | Utilizado para apagar permanentemente algum diretório vazio. | `rmdir *nome-da-pasta*` |
| **rm** | Utilizado para apagar permanentemente algum diretório ouu arquivo. | `rm -r <nome-da-pasta>` |
| **mkdir** | Utilizado para criar um novo. [ **diretório / pasta** ] | `mkdir <nome-da-pasta>` |
| **touch** | Utilizado para criar arquivos com qualquer extensão. | `touch arquivo.txt` |
| **grep** | Procura por padrões e destaca em cores a palavra que o usuário especificar. | `grep "Linux" arquivo.txt` |
| **tar -czvf** | Compacta arquivos. | `tar -czvf arq.tar.gz pasta/` |
|s **tar -xzvf** | Descompacta arquivos. | `tar -xzvf arq.tar.gz` |

### 1.1.3 - Permições e controle de usuários

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
| **sudo** | Serve para executar comandos como administrador. | `sudo apt update` |
| **sudo su**   | Entra no modo superusuário para executar ações com permissão elevada. Pode ser usado para editar um arquivo protegido. | `sudo su` |
| **chmod** | Permite definir quais usuários ou grupos têm permissões específicas para ler, gravar ou executar o arquivo. | `chmod 755 script.sh` |
| **chown** | Ele permite que você atribua um novo proprietário e/ou grupo a um arquivo ou diretório. | `chown root:root /etc/hosts` |
| **adduser** | Cria novo usuário. | `adduser maria` |
| **passwd** | Altera senha. | `passwd` |
| **deluser** | Remove usuário. | `deluser maria` |
| **groups** | Mostra grupos do usuário. | `groups` |

### 1.1.4 - Gerenciamento de pacotes e serviço

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
| **systemctl** | É usado para gerenciar e controlar serviços do sistema. | `systemctl start nginx` |
| **journalctl** | Serve para visualizar e filtrar o registro do sistema, que é armazenado no sistema de registro do journald. | `journalctl -u nginx` |
| **apt** | (Advancedo Package Tool) Usado para gerenciar pacotes de software. | `sudo apt update` |
| **service** | Permite iniciar, parar, reiniciar e verificar o status de serviços específicos. | `service apache2 start` |

### 1.1.5 - Terminal

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
| **history** | Mostra o histórico de comandos utilizados no terminal. | `history` |
| **clear** | Limpa o terminal. | `clear` |
| **exit** | encerra a sessão atual no terminal. | `exit` |
| **tmux** | Usado para criar e gerenciar sessões de terminal em múltiplas janelas ou em um único terminal. | `tmux new-session` |

### 1.1.6 - Rede

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
| **ifconfig** | Configuração de rede. | `ifconfig` |
| **ip addr** | Mostra IPs da máquina. | `ip addr show` |
| **ping** | Testa conectividade. | `ping google.com` |
| **wget** | Baixa arquivos. | `wget url` |
| **curl** | Requisições HTTP.	| `curl http://site.com` |
| **ssh** | Conecta via SSH. | `ssh user@servidor` |
| **scp**	| Copia via SSH.	| `scp arq user@servidor:/tmp` |
| **netstat** | Exibe informações sobre conexões de rede. | `netstat -r` |
| **traceroute** | Mostra o caminho da rede até um destino. | `traceroute github.com` |
| **dig** | fazer consultas DNS (Domain Name System) e obter informações sobre domínios e endereços IP. | `dig google.com` |
| **nmap** | Serve para realizar escaneamentos de rede e obter informações sobre os dispositivos conectados a uma rede. | `nmap 192.168.1.1` |

### 1.1.7 - Logs e monitoramento

| COMANDO | O QUE FAZ | EXEMPLO |
|-------- | --------- | ------- |
| **tail -f** | É usado no para exibir o final de um arquivo ou a saída de um comando em tempo real. | `tail -f arquivo` |
| **watch** | Exibe a saída de um comando em tempo real, atualizando a cada intervalo de tempo especificado. | `watch -n 1 top` |

### 1.1.8 - Deploy e backup

| COMANDO | O QUE FAZ | EXEMPLO |
| ------- | --------- | ------- |
|**rsync** | Sincroniza arquivos e diretórios entre diferentes sistemas ou locais. | `rsync -av origem destino` |
| **rsnapshot** | Permite fazer backups automáticos de volumes de arquivos usando o sistema de backup rsync. | `rsnapshot -c rsnapshot.conf` |
| **dd** | Cria cópias exatas de discos, partições ou pendrives. | `sudo dd if=/dev/sda of=/mnt/backup/disk.img bs=4M status=progress` |
| **mysqldump** | Faz backup de bancos de dados MySQL/MariaDB, exportando todas as tabelas para um arquivo .sql. | `mysqldump -u root -p meu_banco > backup_banco.sql` |

## 1.2. Atalhos do `terminal`

| ATALHO           | O QUE ELE FAZ                                         |
| ---------------- | ----------------------------------------------------- |
| `CTRL + ALT + T` | Abre o terminal linux                                 |
| `CTRL + C`       | Cancela o comando atual em funcionamento              |
| `CTRL + W`       | Apaga a palavra digitada da linha de comando          |
| `CTRL + U`       | Apaga a linha inteira                                 |
| `CTRL + L`       | equivalente ao comando `clear`, limpa a tela          |
| `CTRL + R`       | Busca um comando recente                              |
| `CTRL + D`       | equivalente ao comando `exit`, encerra a sessão atual |

## 1.3 Editor de texto `(nano)`

| ATALHO           | O QUE ELE FAZ                                         |
| ---------------- | --------------------------------------------------------------------- |
| `nano + enter`   | Abre o editor vazio para criar o arquivo   |
| `CTRL + O`       |  Salva o arquivo            |
| `CTRL + X`       |  Sai do editor         |
| `CTRL + R`       | Cópia dados de um arquivo para outro  |
| `nano + nome`    |  Abre o editor para editar o arquivo          |
| `ALT + A`        |  Permite você selecionar a linha a ser copiada      |
| `ALT + 6`        | Permite você copiar a linha selecionada |
| `CTRL + U`        | Cola os dados selecionados anteriormente |
| `CTRL + K`        | Recorta os dados selecionados anteriormente |
| `ALT + /`        | Vai até o final do arquivo |
| `ALT + \`        | Vai até o início do arquivo |
| `ALT + G`        | Vai até a linha especificada do arquivo |
| `CTRL + W`        |  Busca por palavras ou sentenças |
| `ALT + R`        | Substitui uma palavra ou sentença |
