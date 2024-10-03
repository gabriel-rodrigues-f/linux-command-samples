
# Biblioteca de Comandos Linux

![Linux Badge](https://img.shields.io/badge/Linux-Commands-blue?logo=linux&style=for-the-badge)
![GitHub](https://img.shields.io/github/license/gabriel-rodrigues-f/linux-command-samples?style=for-the-badge)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge)

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
