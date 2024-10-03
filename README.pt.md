
# Biblioteca de Comandos Linux

![Linux Badge](https://img.shields.io/badge/Linux-Commands-blue?logo=linux&style=for-the-badge)
![GitHub](https://img.shields.io/github/license/gabriel-rodrigues-f/linux-command-samples?style=for-the-badge)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge)

- [Biblioteca de Comandos Linux](#biblioteca-de-comandos-linux)
  - [📂 1. Navegação e Manipulação de Arquivos](#-1-navegação-e-manipulação-de-arquivos)
    - [🗂️ `ls` - Lista Arquivos e Diretórios](#️-ls---lista-arquivos-e-diretórios)
    - [📁 `cd` - Muda o Diretório Atual](#-cd---muda-o-diretório-atual)
    - [📝 `pwd` - Exibe o Diretório Atual](#-pwd---exibe-o-diretório-atual)
    - [📑 `cp` - Copia Arquivos ou Diretórios](#-cp---copia-arquivos-ou-diretórios)
    - [🔄 `mv` - Move ou Renomeia Arquivos](#-mv---move-ou-renomeia-arquivos)
    - [🗑️ `rm` - Remove Arquivos ou Diretórios](#️-rm---remove-arquivos-ou-diretórios)
    - [📂 `mkdir` - Cria Diretórios](#-mkdir---cria-diretórios)
    - [📝 `touch` - Cria Arquivos](#-touch---cria-arquivos)
  - [✏️ 2. Manipulação de Texto](#️-2-manipulação-de-texto)
    - [🔍 `grep` - Busca em Arquivos de Texto](#-grep---busca-em-arquivos-de-texto)
    - [✂️ `awk` - Processa Texto](#️-awk---processa-texto)
    - [✒️ `sed` - Editor de Fluxo](#️-sed---editor-de-fluxo)
  - [📦 3. Compressão e Arquivamento](#-3-compressão-e-arquivamento)
    - [📚 `tar` - Arquivamento de Arquivos](#-tar---arquivamento-de-arquivos)
  - [⚙️ 4. Sistema e Rede](#️-4-sistema-e-rede)
    - [📊 `ps` - Status de Processos](#-ps---status-de-processos)
    - [🖥️ `top` - Monitor de Processos](#️-top---monitor-de-processos)
    - [🚫 `kill` - Finaliza Processos](#-kill---finaliza-processos)
- [Exemplos de Shell Scripts Úteis para o Dia a Dia](#exemplos-de-shell-scripts-úteis-para-o-dia-a-dia)
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

📘 Este repositório contém uma coleção detalhada de comandos Linux, incluindo descrições das siglas utilizadas, exemplos simples de uso e exemplos de comandos combinados. Este é um guia útil para iniciantes e usuários avançados do sistema operacional Linux.

## 📂 1. Navegação e Manipulação de Arquivos

### 🗂️ `ls` - Lista Arquivos e Diretórios
- **Descrição**: Lista o conteúdo de diretórios.
- **Opções**:
  - `-l`: **long** - Lista arquivos em formato detalhado.
  - `-a`: **all** - Lista todos os arquivos, incluindo ocultos.
  - `-h`: **human-readable** - Mostra tamanhos em formato legível (KB, MB, etc.).
- **Exemplos**:
  ```bash
  ls -l
  ls -a
  ls -lh
  ```

### 📁 `cd` - Muda o Diretório Atual
- **Descrição**: Muda o diretório de trabalho.
- **Exemplos**:
  ```bash
  cd /home/user
  cd ..  # Volta para o diretório pai
  ```

### 📝 `pwd` - Exibe o Diretório Atual
- **Descrição**: Mostra o caminho completo do diretório de trabalho atual.
- **Exemplos**:
  ```bash
  pwd
  ```

### 📑 `cp` - Copia Arquivos ou Diretórios
- **Descrição**: Copia arquivos ou diretórios.
- **Opções**:
  - `-r`: **recursive** - Copia diretórios e seu conteúdo recursivamente.
  - `-i`: **interactive** - Pede confirmação antes de sobrescrever.
  - `-v`: **verbose** - Mostra o que está sendo copiado.
- **Exemplos**:
  ```bash
  cp arquivo.txt /home/user/destino/
  cp -r pasta_origem pasta_destino
  ```

### 🔄 `mv` - Move ou Renomeia Arquivos
- **Descrição**: Move ou renomeia arquivos e diretórios.
- **Opções**:
  - `-i`: **interactive** - Pede confirmação antes de mover/sobrescrever.
  - `-v`: **verbose** - Mostra o que está sendo movido.
- **Exemplos**:
  ```bash
  mv arquivo.txt /home/user/destino/
  mv arquivo.txt novo_nome.txt
  ```

### 🗑️ `rm` - Remove Arquivos ou Diretórios
- **Descrição**: Remove arquivos e diretórios.
- **Opções**:
  - `-r`: **recursive** - Remove diretórios e todo o seu conteúdo.
  - `-f`: **force** - Remove arquivos sem solicitar confirmação.
- **Exemplos**:
  ```bash
  rm arquivo.txt
  rm -rf pasta/
  ```

### 📂 `mkdir` - Cria Diretórios
- **Descrição**: Cria um ou mais diretórios.
- **Opções**:
  - `-p`: **parents** - Cria diretórios pai que não existam.
- **Exemplos**:
  ```bash
  mkdir nova_pasta
  mkdir -p pasta/pai/subpasta
  ```

### 📝 `touch` - Cria Arquivos
- **Descrição**: Cria arquivos vazios ou atualiza a data de modificação.
- **Exemplos**:
  ```bash
  touch novo_arquivo.txt
  ```

## ✏️ 2. Manipulação de Texto

### 🔍 `grep` - Busca em Arquivos de Texto
- **Descrição**: Procura padrões dentro de arquivos de texto.
- **Opções**:
  - `-i`: **ignore-case** - Ignora maiúsculas e minúsculas.
  - `-r`: **recursive** - Busca em todos os arquivos de um diretório.
- **Exemplos**:
  ```bash
  grep "termo" arquivo.txt
  grep -i "termo" arquivo.txt
  ```

### ✂️ `awk` - Processa Texto
- **Descrição**: Manipula e processa textos, especialmente linhas e colunas.
- **Exemplos**:
  ```bash
  awk '{print $1}' arquivo.txt  # Mostra a primeira coluna de cada linha
  ```

### ✒️ `sed` - Editor de Fluxo
- **Descrição**: Realiza substituições em arquivos de texto.
- **Opções**:
  - `-i`: **in-place** - Edita o arquivo diretamente.
- **Exemplos**:
  ```bash
  sed 's/antigo/novo/g' arquivo.txt
  sed -i 's/foo/bar/g' arquivo.txt
  ```

## 📦 3. Compressão e Arquivamento

### 📚 `tar` - Arquivamento de Arquivos
- **Descrição**: Cria ou extrai arquivos `.tar`.
- **Opções**:
  - `-c`: **create** - Cria um novo arquivo tar.
  - `-x`: **extract** - Extrai o conteúdo de um arquivo tar.
  - `-z`: **gzip** - Compacta/descompacta usando gzip.
  - `-f`: **file** - Especifica o nome do arquivo.
- **Exemplos**:
  ```bash
  tar -czf arquivo.tar.gz pasta/
  tar -xzf arquivo.tar.gz
  ```

## ⚙️ 4. Sistema e Rede

### 📊 `ps` - Status de Processos
- **Descrição**: Mostra uma lista dos processos em execução.
- **Opções**:
  - `-e`: **every** - Mostra todos os processos.
  - `-f`: **full-format** - Mostra detalhes completos.
- **Exemplos**:
  ```bash
  ps -ef
  ```

### 🖥️ `top` - Monitor de Processos
- **Descrição**: Exibe processos em execução em tempo real.
- **Exemplos**:
  ```bash
  top
  ```

### 🚫 `kill` - Finaliza Processos
- **Descrição**: Envia um sinal para finalizar processos.
- **Opções**:
  - `-9`: **SIGKILL** - Mata o processo imediatamente.
- **Exemplos**:
  ```bash
  kill -9 1234  # Mata o processo de ID 1234
  ```
</br>
</br>
</br>
</br>

# Exemplos de Shell Scripts Úteis para o Dia a Dia

Este repositório contém exemplos de scripts shell úteis para automatizar tarefas diárias no Linux. Cada exemplo descreve um caso prático, como criar um script para realizar uma tarefa comum.

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



