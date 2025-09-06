## The tar command in Linux is used for archiving and compressing files and directories. It’s one of the most commonly used commands for backups and transferring multiple files as a single package.

## Basic Syntax
tar [options] archive_name.tar files_or_directories

archive_name.tar → name of the archive to create or extract

files_or_directories → files/folders to include

## 📌 Common Options

| Option | Meaning                         |
| ------ | ------------------------------- |
| `c`    | Create a new archive            |
| `x`    | Extract an archive              |
| `t`    | List contents of an archive     |
| `v`    | Verbose (show progress)         |
| `f`    | Specify filename of the archive |
| `z`    | Compress/Decompress with gzip   |
| `j`    | Compress/Decompress with bzip2  |
| `J`    | Compress/Decompress with xz     |

## 📌 Examples
## 1. Create a tar archive
tar -cvf backup.tar file1.txt file2.txt

c → create
v → verbose
f → filename

## 2. Create a tar.gz archive (gzip compression)
tar -czvf backup.tar.gz folder/

z → gzip compression
Result: compressed archive backup.tar.gz

## 3. List Contents of an Archive
tar -tvf backup.tar
tar -tzvf backup.tar.gz   # for gzip compressed

t → list
v → verbose
f → filename

## 4.Extract an Archive
tar -xvf backup.tar
tar -xzvf backup.tar.gz   # gzip compressed
tar -xjvf backup.tar.bz2  # bzip2 compressed

x → extract

## 5.Extract to a Specific Directory
tar -xvf backup.tar -C /home/krishna/restore/

-C → extract files into the given directory

## The gzip command in Linux is used for compressing files. It reduces the file size by using GNU zip compression, making it easier to store or transfer files.

## Basic Usage
## 1. Compress a File
gzip file.txt

Compresses file.txt → result: file.txt.gz

Original file is replaced by the compressed file.

## 2. Keep Original File

gzip -c file.txt > file.txt.gz

-c → write output to stdout

Original file.txt remains intact.

## 3. Compress Multiple Files
gzip file1.txt file2.txt

Compresses each file individually → file1.txt.gz, file2.txt.gz

Note: gzip does not combine multiple files into one (use tar + gzip for that).

## 4. Decompress a File
gzip -d file.txt.gz

or

gunzip file.txt.gz


Restores the original file (file.txt)

