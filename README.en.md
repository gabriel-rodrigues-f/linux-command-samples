
# Linux Command Library

![Linux Badge](https://img.shields.io/badge/Linux-Commands-blue?logo=linux&style=for-the-badge)
![GitHub](https://img.shields.io/github/license/gabriel-rodrigues-f/linux-command-samples?style=for-the-badge)
![Contributions Welcome](https://img.shields.io/badge/Contributions-Welcome-brightgreen?style=for-the-badge)

- [Linux Command Library](#linux-command-library)
  - [📂 1. Navigation and File Management](#-1-navigation-and-file-management)
    - [🗂️ `ls` - List Files and Directories](#️-ls---list-files-and-directories)
    - [📁 `cd` - Change Current Directory](#-cd---change-current-directory)
    - [📝 `pwd` - Display Current Directory](#-pwd---display-current-directory)
    - [📑 `cp` - Copy Files or Directories](#-cp---copy-files-or-directories)
    - [🔄 `mv` - Move or Rename Files](#-mv---move-or-rename-files)
    - [🗑️ `rm` - Remove Files or Directories](#️-rm---remove-files-or-directories)
    - [📂 `mkdir` - Create Directories](#-mkdir---create-directories)
    - [📝 `touch` - Create Files](#-touch---create-files)
  - [✏️ 2. Text Manipulation](#️-2-text-manipulation)
    - [🔍 `grep` - Search in Text Files](#-grep---search-in-text-files)
    - [✂️ `awk` - Process Text](#️-awk---process-text)
    - [✒️ `sed` - Stream Editor](#️-sed---stream-editor)
  - [📦 3. Compressão e Arquivamento](#-3-compressão-e-arquivamento)
    - [📚 `tar` - Archive Files](#-tar---archive-files)
  - [⚙️ 4. System and Network](#️-4-system-and-network)
    - [📊 `ps` - Process Status](#-ps---process-status)
    - [🖥️ `top` - Process Monitor](#️-top---process-monitor)
    - [🚫 `kill` - Kill Processes](#-kill---kill-processes)
  - [2. 💾 Automatic Daily Backup](#2--automatic-daily-backup)
  - [3. 📊 Monitor CPU Usage](#3--monitor-cpu-usage)
  - [4. 🗃️ Find and Compress Old Files](#4-️-find-and-compress-old-files)
  - [5. ✏️ Replace Text in Multiple Files](#5-️-replace-text-in-multiple-files)
  - [6. 🌐 Submit the Output of a Command to a File](#6--submit-the-output-of-a-command-to-a-file)
  - [7. ⏰ Run a Command Based on a Time](#7--run-a-command-based-on-a-time)
  - [8. 📄 Count Lines in Text Files](#8--count-lines-in-text-files)
  - [9. 🔌 Check Connection to a Host](#9--check-connection-to-a-host)
  - [10. 🗑️ Remove Temporary Files](#10-️-remove-temporary-files)

📘 This repository contains a detailed collection of Linux commands, including descriptions of flags used, simple usage examples, and combined command examples. It serves as a useful guide for both beginners and advanced users of the Linux operating system.

## 📂 1. Navigation and File Management

### 🗂️ `ls` - List Files and Directories
- **Description**: Lists the content of directories.
- **Options**:
  - `-l`: **long** - Lists files in detailed format.
  - `-a`: **all** - Lists all files, including hidden ones.
  - `-h`: **human-readable** - Shows sizes in human-readable format (KB, MB, etc.).
- **Examples**:
  ```bash
  ls -l
  ls -a
  ls -lh
  ```

### 📁 `cd` - Change Current Directory
- **Description**: Changes the working directory.
- **Examples**:
  ```bash
  cd /home/user
  cd ..  # Goes back to the parent directory
  ```

### 📝 `pwd` - Display Current Directory
- **Description**: Displays the full path of the current working directory.
- **Examples**:
  ```bash
  pwd
  ```

### 📑 `cp` - Copy Files or Directories
- **Description**: Copies files or directories.
- **Options**:
  - `-r`: **recursive** - Copies directories and their content recursively.
  - `-i`: **interactive** - Asks for confirmation before overwriting.
  - `-v`: **verbose** - Displays what is being copied.
- **Examples**:
  ```bash
  cp file.txt /home/user/destination/
  cp -r source_folder destination_folder
  ```

### 🔄 `mv` - Move or Rename Files
- **Description**: Moves or renames files and directories.
- **Options**:
  - `-i`: **interactive** - Asks for confirmation before moving/overwriting.
  - `-v`: **verbose** - Displays what is being moved.
- **Examples**:
  ```bash
  mv file.txt /home/user/destination/
  mv file.txt new_name.txt
  ```

### 🗑️ `rm` - Remove Files or Directories
- **Description**: Removes files and directories.
- **Options**:
  - `-r`: **recursive** - Removes directories and all their content.
  - `-f`: **force** - Removes files without asking for confirmation.
- **Examples**:
  ```bash
  rm file.txt
  rm -rf folder/
  ```

### 📂 `mkdir` - Create Directories
- **Description**: Creates one or more directories.
- **Options**:
  - `-p`: **parents** - Creates parent directories if they do not exist.
- **Examples**:
  ```bash
  mkdir new_folder
  mkdir -p parent_folder/subfolder
  ```

### 📝 `touch` - Create Files
- **Description**: Creates empty files or updates the modification date.
- **Examples**:
  ```bash
  touch new_file.txt
  ```

## ✏️ 2. Text Manipulation

### 🔍 `grep` - Search in Text Files
- **Description**: Searches for patterns within text files.
- **Options**:
  - `-i`: **ignore-case** - Ignores case distinctions.
  - `-r`: **recursive** - Searches in all files within a directory.
- **Examples**:
  ```bash
  grep "term" file.txt
  grep -i "term" file.txt
  ```

### ✂️ `awk` - Process Text
- **Description**: Manipulates and processes text, especially lines and columns.
- **Examples**:
  ```bash
  awk '{print $1}' file.txt  # Prints the first column of each line
  ```

### ✒️ `sed` - Stream Editor
- **Description**: Performs text substitutions within files.
- **Options**:
  - `-i`: **in-place** - Edits the file directly.
- **Examples**:
  ```bash
  sed 's/old/new/g' file.txt
  sed -i 's/foo/bar/g' file.txt
  ```

## 📦 3. Compressão e Arquivamento
### 📚 `tar` - Archive Files
- **Description**: Creates or extracts `.tar` files.
- **Options**:
- `-c`: **create** - Creates a new tar file.
- `-x`: **extract** - Extracts the contents of a tar file.
- `-z`: **gzip** - Compresses/decompresses using gzip.
- `-f`: **file** - Specifies the file name.
- **Examples**:
```bash
tar -czf file.tar.gz folder/
tar -xzf file.tar.gz
```

## ⚙️ 4. System and Network

### 📊 `ps` - Process Status
- **Description**: Shows a list of running processes.
- **Options**:
- `-e`: **every** - Shows all processes.
- `-f`: **full-format** - Shows full details.
- **Examples**:
```bash
ps -ef
```

### 🖥️ `top` - Process Monitor
- **Description**: Displays running processes in real time.
- **Examples**:
```bash
top
```

### 🚫 `kill` - Kill Processes
- **Description**: Sends a signal to kill processes.
- **Options**:
- `-9`: **SIGKILL** - Kills the process immediately.
- **Examples**:
```bash
kill -9 1234 # Kills the process with ID 1234

# Examples of Useful Shell Scripts for Everyday Use

This repository contains examples of useful shell scripts for automating everyday tasks in Linux. Each example describes a practical case, such as creating a script to perform a common task.

## 1. 📦 Compress a Directory

To compress a specific directory into a `.tar.gz` file, create a file called `compress.sh`:

```bash
#!/bin/bash
echo "Enter the name of the directory to compress:"
read directory
tar -czf ${directory}.tar.gz $directory
echo "Directory $directory compressed to ${directory}.tar.gz"
```

## 2. 💾 Automatic Daily Backup

To create a daily backup of the `/home/user` directory, create a file called `daily_backup.sh`:

```bash
#!/bin/bash
directory="/home/user"
backup_name="backup_$(date +%Y%m%d).tar.gz"
tar -czf /backup/$backup_name $directory
echo "Backup from the created $directory directory: /backup/$backup_name"
```

## 3. 📊 Monitor CPU Usage

To monitor CPU usage and save the results in a log, create a file called `monitor_cpu.sh`:

```bash
#!/bin/bash
top -b -n 1 | head -n 10 >> /home/user/cpu_usage.log
echo "CPU usage recorded in /home/user/cpu_usage.log"
```

## 4. 🗃️ Find and Compress Old Files

To find files older than 7 days and compress them, create a file called `compress_old.sh`:

```bash
#!/bin/bash
find /home/user -type f -mtime +7 | tar -czf old_files_$(date +%Y%m%d).tar.gz -T -
echo "Old files compressed in old_files_$(date +%Y%m%d).tar.gz"
```

## 5. ✏️ Replace Text in Multiple Files

To replace all occurrences of a specific term in multiple `.txt` files, create a file called `replace_text.sh`:

```bash
#!/bin/bash
echo "Enter the term to be replaced:"
read old_term
echo "Enter the new term:"
read new_term
sed -i "s/$old_term/$new_term/g" *.txt
echo "Term $old_term replaced by $new_term in all .txt files"
```

## 6. 🌐 Submit the Output of a Command to a File

To send the output of the `curl` command to a `.txt` file, create a file called `curl_to_file.sh`:

```bash
#!/bin/bash
echo "Enter the URL to access:"
read url
curl $url > output.txt
echo "Output saved in output.txt"
```

## 7. ⏰ Run a Command Based on a Time

To schedule a command to run at 2:00 AM, create a file called `schedule_backup.sh`:

```bash
#!/bin/bash
(crontab -l ; echo "0 2 * * * /home/user/daily_backup.sh") | crontab -
echo "Backup scheduled to run daily at 2am"
```

## 8. 📄 Count Lines in Text Files

To count the number of lines in all `.log` files in a directory, create a file called `count_lines.sh`:

```bash
#!/bin/bash
for file in *.log; do
lines=$(wc -l < ​​$file)
echo "$file: $lines lines"
done
```

## 9. 🔌 Check Connection to a Host

To check connectivity to a specific host using `ping`, create a file called `check_connection.sh`:

```bash
#!/bin/bash
echo "Enter the address of the host to be checked:"
read host
ping -c 4 $host
```

## 10. 🗑️ Remove Temporary Files

To remove all temporary files (`*.tmp`) from a directory, create a file called `remove_tmp.sh`:

```bash
#!/bin/bash
echo "Removing temporary files from the current directory..."
rm -f *.tmp
echo "Temporary files removed."
```

---