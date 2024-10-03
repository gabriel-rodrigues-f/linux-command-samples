
# Biblioteca de Comandos de Linux

![Linux Badge](https://img.shields.io/badge/Linux-Commands-blue?logo=linux&style=for-the-badge)
![GitHub](https://img.shields.io/github/license/gabriel-rodrigues-f/linux-command-samples?style=for-the-badge)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge)

- [Biblioteca de Comandos de Linux](#biblioteca-de-comandos-de-linux)
  - [📂 1. Navegación y Gestión de Archivos](#-1-navegación-y-gestión-de-archivos)
    - [🗂️ `ls` - Listar Archivos y Directorios](#️-ls---listar-archivos-y-directorios)
    - [📁 `cd` - Cambiar el Directorio Actual](#-cd---cambiar-el-directorio-actual)
    - [📝 `pwd` - Mostrar el Directorio Actual](#-pwd---mostrar-el-directorio-actual)
    - [📑 `cp` - Copiar Archivos o Directorios](#-cp---copiar-archivos-o-directorios)
    - [🔄 `mv` - Mover o Renombrar Archivos](#-mv---mover-o-renombrar-archivos)
    - [🗑️ `rm` - Eliminar Archivos o Directorios](#️-rm---eliminar-archivos-o-directorios)
    - [📂 `mkdir` - Crear Directorios](#-mkdir---crear-directorios)
    - [📝 `touch` - Crear Archivos](#-touch---crear-archivos)
  - [✏️ 2. Manipulación de Texto](#️-2-manipulación-de-texto)
    - [🔍 `grep` - Buscar en Archivos de Texto](#-grep---buscar-en-archivos-de-texto)
    - [✂️ `awk` - Procesar Texto](#️-awk---procesar-texto)
    - [✒️ `sed` - Editor de Flujo](#️-sed---editor-de-flujo)
  - [📦 3. Compresión y Archivado](#-3-compresión-y-archivado)
    - [📚 `tar` - Archivar Archivos](#-tar---archivar-archivos)
  - [⚙️ 4. Sistema y Red](#️-4-sistema-y-red)
    - [📊 `ps` - Estado de Procesos](#-ps---estado-de-procesos)
    - [🖥️ `top` - Monitor de Procesos](#️-top---monitor-de-procesos)
    - [🚫 `kill` - Finalizar Procesos](#-kill---finalizar-procesos)
- [Ejemplos de Scripts Shell Útiles para el Uso Diario](#ejemplos-de-scripts-shell-útiles-para-el-uso-diario)
  - [1. 📦 Comprimir un Directorio](#1--comprimir-un-directorio)
  - [2. 💾 Copia de Seguridad Automática Diaria](#2--copia-de-seguridad-automática-diaria)
  - [3. 📊 Monitorizar el Uso de la CPU](#3--monitorizar-el-uso-de-la-cpu)
  - [4. 🗃️ Encontrar y Comprimir Archivos Antiguos](#4-️-encontrar-y-comprimir-archivos-antiguos)
  - [5. ✏️ Reemplazar Texto en Múltiples Archivos](#5-️-reemplazar-texto-en-múltiples-archivos)
  - [6. 🌐 Enviar el Resultado de un Comando a un Archivo](#6--enviar-el-resultado-de-un-comando-a-un-archivo)
  - [7. ⏰ Ejecutar un Comando en Función del Tiempo](#7--ejecutar-un-comando-en-función-del-tiempo)
  - [8. 📄 Contar Líneas en Archivos de Texto](#8--contar-líneas-en-archivos-de-texto)
  - [9. 🔌 Verificar Conexión con un Host](#9--verificar-conexión-con-un-host)
  - [10. 🗑️ Eliminar Archivos Temporales](#10-️-eliminar-archivos-temporales)

📘 Este repositorio contiene una colección detallada de comandos de Linux, incluyendo descripciones de las banderas utilizadas, ejemplos de uso simple y ejemplos de comandos combinados. Es una guía útil tanto para principiantes como para usuarios avanzados del sistema operativo Linux.

## 📂 1. Navegación y Gestión de Archivos

### 🗂️ `ls` - Listar Archivos y Directorios
- **Descripción**: Lista el contenido de los directorios.
- **Opciones**:
  - `-l`: **long** - Lista archivos en formato detallado.
  - `-a`: **all** - Lista todos los archivos, incluidos los ocultos.
  - `-h`: **human-readable** - Muestra los tamaños en un formato legible (KB, MB, etc.).
- **Ejemplos**:
  ```bash
  ls -l
  ls -a
  ls -lh
  ```

### 📁 `cd` - Cambiar el Directorio Actual
- **Descripción**: Cambia el directorio de trabajo.
- **Ejemplos**:
  ```bash
  cd /home/user
  cd ..  # Vuelve al directorio padre
  ```

### 📝 `pwd` - Mostrar el Directorio Actual
- **Descripción**: Muestra la ruta completa del directorio de trabajo actual.
- **Ejemplos**:
  ```bash
  pwd
  ```

### 📑 `cp` - Copiar Archivos o Directorios
- **Descripción**: Copia archivos o directorios.
- **Opciones**:
  - `-r`: **recursive** - Copia directorios y su contenido recursivamente.
  - `-i`: **interactive** - Pide confirmación antes de sobrescribir.
  - `-v`: **verbose** - Muestra lo que está siendo copiado.
- **Ejemplos**:
  ```bash
  cp file.txt /home/user/destination/
  cp -r source_folder destination_folder
  ```

### 🔄 `mv` - Mover o Renombrar Archivos
- **Descripción**: Mueve o renombra archivos y directorios.
- **Opciones**:
  - `-i`: **interactive** - Pide confirmación antes de mover/sobrescribir.
  - `-v`: **verbose** - Muestra lo que está siendo movido.
- **Ejemplos**:
  ```bash
  mv file.txt /home/user/destination/
  mv file.txt new_name.txt
  ```

### 🗑️ `rm` - Eliminar Archivos o Directorios
- **Descripción**: Elimina archivos y directorios.
- **Opciones**:
  - `-r`: **recursive** - Elimina directorios y todo su contenido.
  - `-f`: **force** - Elimina archivos sin pedir confirmación.
- **Ejemplos**:
  ```bash
  rm file.txt
  rm -rf folder/
  ```

### 📂 `mkdir` - Crear Directorios
- **Descripción**: Crea uno o más directorios.
- **Opciones**:
  - `-p`: **parents** - Crea los directorios padre que no existan.
- **Ejemplos**:
  ```bash
  mkdir new_folder
  mkdir -p parent_folder/subfolder
  ```

### 📝 `touch` - Crear Archivos
- **Descripción**: Crea archivos vacíos o actualiza la fecha de modificación.
- **Ejemplos**:
  ```bash
  touch new_file.txt
  ```

## ✏️ 2. Manipulación de Texto

### 🔍 `grep` - Buscar en Archivos de Texto
- **Descripción**: Busca patrones dentro de archivos de texto.
- **Opciones**:
  - `-i`: **ignore-case** - Ignora mayúsculas y minúsculas.
  - `-r`: **recursive** - Busca en todos los archivos de un directorio.
- **Ejemplos**:
  ```bash
  grep "term" file.txt
  grep -i "term" file.txt
  ```

### ✂️ `awk` - Procesar Texto
- **Descripción**: Manipula y procesa texto, especialmente líneas y columnas.
- **Ejemplos**:
  ```bash
  awk '{print $1}' file.txt  # Imprime la primera columna de cada línea
  ```

### ✒️ `sed` - Editor de Flujo
- **Descripción**: Realiza sustituciones de texto dentro de archivos.
- **Opciones**:
  - `-i`: **in-place** - Edita el archivo directamente.
- **Ejemplos**:
  ```bash
  sed 's/old/new/g' file.txt
  sed -i 's/foo/bar/g' file.txt
  ```

## 📦 3. Compresión y Archivado

### 📚 `tar` - Archivar Archivos
- **Descripción**: Crea o extrae archivos `.tar`.
- **Opciones**:
  - `-c`: **create** - Crea un nuevo archivo tar.
  - `-x`: **extract** - Extrae el contenido de un archivo tar.
  - `-z`: **gzip** - Comprime/descomprime usando gzip.
  - `-f`: **file** - Especifica el nombre del archivo.
- **Ejemplos**:
  ```bash
  tar -czf file.tar.gz folder/
  tar -xzf file.tar.gz
  ```

## ⚙️ 4. Sistema y Red

### 📊 `ps` - Estado de Procesos
- **Descripción**: Muestra una lista de los procesos en ejecución.
- **Opciones**:
  - `-e`: **every** - Muestra todos los procesos.
  - `-f`: **full-format** - Muestra detalles completos.
- **Ejemplos**:
  ```bash
  ps -ef
  ```

### 🖥️ `top` - Monitor de Procesos
- **Descripción**: Muestra procesos en ejecución en tiempo real.
- **Ejemplos**:
  ```bash
  top
  ```

### 🚫 `kill` - Finalizar Procesos
- **Descripción**: Envía una señal para finalizar procesos.
- **Opciones**:
  - `-9`: **SIGKILL** - Mata el proceso inmediatamente.
- **Ejemplos**:
  ```bash
  kill -9 1234 # Mata el proceso con ID 1234
  ```

# Ejemplos de Scripts Shell Útiles para el Uso Diario

Este repositorio contiene ejemplos de scripts shell útiles para automatizar tareas diarias en Linux. Cada ejemplo describe un caso práctico, como crear un script para realizar una tarea común.

## 1. 📦 Comprimir un Directorio

Para comprimir un directorio específico en un archivo `.tar.gz`, cree un archivo llamado `compress.sh`:

```bash
#!/bin/bash
echo "Ingrese el nombre del directorio a comprimir:"
read directory
tar -czf ${directory}.tar.gz $directory
echo "Directorio $directory comprimido en ${directory}.tar.gz"
```

## 2. 💾 Copia de Seguridad Automática Diaria

Para crear una copia de seguridad diaria del directorio `/home/user`, cree un archivo llamado `daily_backup.sh`:

```bash
#!/bin/bash
directory="/home/user"
backup_name="backup_$(date +%Y%m%d).tar.gz"
tar -czf /backup/$backup_name $directory
echo "Copia de seguridad del directorio creado $directory: /backup/$backup_name"
```

## 3. 📊 Monitorizar el Uso de la CPU

Para monitorizar el uso de la CPU y guardar los resultados en un log, cree un archivo llamado `monitor_cpu.sh`:

```bash
#!/bin/bash
top -b -n 1 | head -n 10 >> /home/user/cpu_usage.log
echo "Uso de CPU registrado en /home/user/cpu_usage.log"
```

## 4. 🗃️ Encontrar y Comprimir Archivos Antiguos

Para encontrar archivos de más de 7 días y comprimirlos, cree un archivo llamado `compress_old.sh`:

```bash
#!/bin/bash
find /home/user -type f -mtime +7 | tar -czf old_files_$(date +%Y%m%d).tar.gz -T -
echo "Archivos antiguos comprimidos en old_files_$(date +%Y%m%d).tar.gz"
```

## 5. ✏️ Reemplazar Texto en Múltiples Archivos

Para reemplazar todas las ocurrencias de un término específico en múltiples archivos `.txt`, cree un archivo llamado `replace_text.sh`:

```bash
#!/bin/bash
echo "Ingrese el término a reemplazar:"
read old_term
echo "Ingrese el nuevo término:"
read new_term
sed -i "s/$old_term/$new_term/g" *.txt
echo "Término $old_term reemplazado por $new_term en todos los archivos .txt"
```

## 6. 🌐 Enviar el Resultado de un Comando a un Archivo

Para enviar el resultado del comando `curl` a un archivo `.txt`, cree un archivo llamado `curl_to_file.sh`:

```bash
#!/bin/bash
echo "Ingrese la URL a acceder:"
read url
curl $url > output.txt
echo "Resultado guardado en output.txt"
```

## 7. ⏰ Ejecutar un Comando en Función del Tiempo

Para programar la ejecución de un comando a las 2:00 AM, cree un archivo llamado `schedule_backup.sh`:

```bash
#!/bin/bash
(crontab -l ; echo "0 2 * * * /home/user/daily_backup.sh") | crontab -
echo "Copia de seguridad programada para ejecutarse diariamente a las 2am"
```

## 8. 📄 Contar Líneas en Archivos de Texto

Para contar el número de líneas en todos los archivos `.log` de un directorio, cree un archivo llamado `count_lines.sh`:

```bash
#!/bin/bash
for file in *.log; do
lines=$(wc -l < $file)
echo "$file: $lines líneas"
done
```

## 9. 🔌 Verificar Conexión con un Host

Para verificar la conectividad con un host específico usando `ping`, cree un archivo llamado `check_connection.sh`:

```bash
#!/bin/bash
echo "Ingrese la dirección del host a verificar:"
read host
ping -c 4 $host
```

## 10. 🗑️ Eliminar Archivos Temporales

Para eliminar todos los archivos temporales (`*.tmp`) de un directorio, cree un archivo llamado `remove_tmp.sh`:

```bash
#!/bin/bash
echo "Eliminando archivos temporales del directorio actual..."
rm -f *.tmp
echo "Archivos temporales eliminados."
```
