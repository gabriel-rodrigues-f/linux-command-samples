
# Exemplos de Shell Scripts Úteis para o Dia a Dia

Este repositório contém exemplos de scripts shell úteis para automatizar tarefas diárias no Linux. Cada exemplo descreve um caso prático, como criar um script para realizar uma tarefa comum.

## 📋 Índice
- [Exemplos de Shell Scripts Úteis para o Dia a Dia](#exemplos-de-shell-scripts-úteis-para-o-dia-a-dia)
  - [📋 Índice](#-índice)
  - [1. 📦 Compactar um Diretório](#1--compactar-um-diretório)
  - [2. 💾 Backup Diário Automático](#2--backup-diário-automático)
  - [3. 📊 Monitorar Utilização de CPU](#3--monitorar-utilização-de-cpu)
  - [4. 🗃️ Encontrar e Compactar Arquivos Antigos](#4-️-encontrar-e-compactar-arquivos-antigos)
  - [5. ✏️ Substituir Texto em Múltiplos Arquivos](#5-️-substituir-texto-em-múltiplos-arquivos)
  - [6. 🌐 Enviar o Resultado de um Comando para um Arquivo](#6--enviar-o-resultado-de-um-comando-para-um-arquivo)
  - [7. ⏰ Executar um Comando com Base no Horário](#7--executar-um-comando-com-base-no-horário)
  - [8. 📄 Contar Linhas em Arquivos de Texto](#8--contar-linhas-em-arquivos-de-texto)
  - [9. 🔌 Verificar Conexão com um Host](#9--verificar-conexão-com-um-host)
  - [10. 🗑️ Remover Arquivos Temporários](#10-️-remover-arquivos-temporários)

## 1. 📦 Compactar um Diretório

Para compactar um diretório específico em um arquivo `.tar.gz`, crie um arquivo chamado `compactar.sh`:

```bash
#!/bin/bash
echo "Digite o nome do diretório a ser compactado:"
read diretorio
tar -czf ${diretorio}.tar.gz $diretorio
echo "Diretório $diretorio compactado para ${diretorio}.tar.gz"
```

## 2. 💾 Backup Diário Automático

Para criar um backup diário do diretório `/home/user`, crie um arquivo chamado `backup_diario.sh`:

```bash
#!/bin/bash
diretorio="/home/user"
backup_nome="backup_$(date +%Y%m%d).tar.gz"
tar -czf /backup/$backup_nome $diretorio
echo "Backup do diretório $diretorio criado: /backup/$backup_nome"
```

## 3. 📊 Monitorar Utilização de CPU

Para monitorar a utilização da CPU e salvar os resultados em um log, crie um arquivo chamado `monitor_cpu.sh`:

```bash
#!/bin/bash
top -b -n 1 | head -n 10 >> /home/user/cpu_usage.log
echo "Utilização da CPU registrada em /home/user/cpu_usage.log"
```

## 4. 🗃️ Encontrar e Compactar Arquivos Antigos

Para encontrar arquivos mais antigos que 7 dias e compactá-los, crie um arquivo chamado `compactar_antigos.sh`:

```bash
#!/bin/bash
find /home/user -type f -mtime +7 | tar -czf arquivos_antigos_$(date +%Y%m%d).tar.gz -T -
echo "Arquivos antigos compactados em arquivos_antigos_$(date +%Y%m%d).tar.gz"
```

## 5. ✏️ Substituir Texto em Múltiplos Arquivos

Para substituir todas as ocorrências de um termo específico em múltiplos arquivos `.txt`, crie um arquivo chamado `substituir_texto.sh`:

```bash
#!/bin/bash
echo "Digite o termo a ser substituído:"
read termo_antigo
echo "Digite o novo termo:"
read termo_novo
sed -i "s/$termo_antigo/$termo_novo/g" *.txt
echo "Termo $termo_antigo substituído por $termo_novo em todos os arquivos .txt"
```

## 6. 🌐 Enviar o Resultado de um Comando para um Arquivo

Para enviar o resultado do comando `curl` para um arquivo `.txt`, crie um arquivo chamado `curl_para_arquivo.sh`:

```bash
#!/bin/bash
echo "Digite a URL a ser acessada:"
read url
curl $url > resultado.txt
echo "Resultado salvo em resultado.txt"
```

## 7. ⏰ Executar um Comando com Base no Horário

Para agendar a execução de um comando às 2h da manhã, crie um arquivo chamado `agendar_backup.sh`:

```bash
#!/bin/bash
(crontab -l ; echo "0 2 * * * /home/user/backup_diario.sh") | crontab -
echo "Backup agendado para ser executado diariamente às 2h"
```

## 8. 📄 Contar Linhas em Arquivos de Texto

Para contar o número de linhas em todos os arquivos `.log` de um diretório, crie um arquivo chamado `contar_linhas.sh`:

```bash
#!/bin/bash
for file in *.log; do
    linhas=$(wc -l < $file)
    echo "$file: $linhas linhas"
done
```

## 9. 🔌 Verificar Conexão com um Host

Para verificar a conectividade com um host específico usando `ping`, crie um arquivo chamado `verificar_conexao.sh`:

```bash
#!/bin/bash
echo "Digite o endereço do host a ser verificado:"
read host
ping -c 4 $host
```

## 10. 🗑️ Remover Arquivos Temporários

Para remover todos os arquivos temporários (`*.tmp`) de um diretório, crie um arquivo chamado `remover_tmp.sh`:

```bash
#!/bin/bash
echo "Removendo arquivos temporários do diretório atual..."
rm -f *.tmp
echo "Arquivos temporários removidos."
```

---

Cada um desses exemplos pode ser modificado para se ajustar às suas necessidades. Esses scripts são uma ótima maneira de começar a automatizar tarefas comuns no Linux, aumentando a produtividade e reduzindo o trabalho manual.
