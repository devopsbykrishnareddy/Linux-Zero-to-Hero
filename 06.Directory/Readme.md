# Directory Commands

## 1. pwd – Print Working Directory
pwd
👉 Example: /home/krishna/Documents

## 2. ls – List Directory Contents
ls        # basic listing
ls -l     # detailed listing
ls -a     # show hidden files
ls -lh    # human-readable sizes

## 3. cd – Change Directory

Move from one directory to another.

cd /home/krishna/Documents   # go to Documents
cd ~                         # go to home directory
cd ..                        # go up one level
cd -                         # go back to previous directory


## 4. mkdir – Make Directory

Create a new directory.

mkdir projects
mkdir -p work/code/python    # create nested directories


## 5. rmdir – Remove Empty Directory
Deletes an empty directory.
rmdir projects

## 6. rm -r – Remove Directory (with contents)

Deletes a directory and all files inside it.

rm -r projects
rm -rf projects   # force delete (be careful!)


## 7. tree (optional, needs installation)
tree


## 8. find – Search for Directories/Files

find /home -type d -name "Documents"

## Quick Summary Table

| Command | Purpose                        |
| ------- | ------------------------------ |
| `pwd`   | Show current directory         |
| `ls`    | List directory contents        |
| `cd`    | Change directory               |
| `mkdir` | Create new directory           |
| `rmdir` | Remove empty directory         |
| `rm -r` | Remove directory with contents |
| `tree`  | Show directory structure       |
| `find`  | Search for directories/files   |

