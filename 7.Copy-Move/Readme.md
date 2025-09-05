# Copy Commands in Linux

## Copy a File
cp file1.txt file2.txt

👉 Copies file1.txt to file2.txt (new file created).

## 2. Copy a File to Another Directory
cp file1.txt /home/krishna/Documents/

👉 Copies file1.txt into the Documents folder (keeping the same name).

## 3. Copy and Rename
cp file1.txt /home/krishna/Documents/newfile.txt


👉 Copies and renames at the destination.

## 4. Copy Multiple Files

cp file1.txt file2.txt /home/krishna/backup/

👉 Copies file1.txt and file2.txt to the backup folder.

## 5. Copy Entire Directory

cp -r project/ /home/krishna/backup/

👉 Copies the whole project folder (recursively).

## 6. Preserve File Attributes
cp -p file1.txt /home/krishna/backup/


👉 Keeps original file permissions, timestamps, and ownership.

## 7. Verbose Output (show what is happening)
cp -v file1.txt /home/krishna/backup/

👉 Displays messages while copying.

## 8. Interactive Copy (ask before overwrite)
cp -i file1.txt /home/krishna/backup/

## 9. Force Copy (overwrite without asking)
cp -f file1.txt /home/krishna/backup/


## Quick Reference Table

| Command Example        | Purpose                         |
| ---------------------- | ------------------------------- |
| `cp file1 file2`       | Copy file1 → file2              |
| `cp file1 /dir/`       | Copy file to directory          |
| `cp file1 file2 /dir/` | Copy multiple files             |
| `cp -r dir1 dir2`      | Copy directory recursively      |
| `cp -p file /dir/`     | Preserve permissions/timestamps |
| `cp -v file /dir/`     | Show progress (verbose)         |
| `cp -i file /dir/`     | Ask before overwrite            |
| `cp -f file /dir/`     | Force overwrite                 |



## The mv command in Linux is used to move or rename files and directories. Unlike cp, it does not keep the original; it transfers the file.

# Move/Rename Commands in Linux

## 1. Move a File to Another Directory
mv file1.txt /home/krishna/Documents/

👉 Moves file1.txt to the Documents folder

## 2. Rename a File
mv oldname.txt newname.txt


👉 Renames oldname.txt to newname.txt.


## 3. Move Multiple Files
mv file1.txt file2.txt /home/krishna/backup/


👉 Moves multiple files into a directory.

## 4. Move a Directory
mv project/ /home/krishna/backup/


👉 Moves the whole project directory.


## 5. Interactive Mode (Ask Before Overwriting)
mv -i file1.txt /home/krishna/Documents/


👉 Prompts before overwriting an existing file.

## 6. Force Move (Overwrite Without Asking)
mv -f file1.txt /home/krishna/Documents/


## 7. Verbose Mode (Show What’s Happening)
mv -v file1.txt /home/krishna/Documents/


## Quick Reference Table

| Command Example        | Purpose                |
| ---------------------- | ---------------------- |
| `mv file /dir/`        | Move file to directory |
| `mv oldname newname`   | Rename file            |
| `mv file1 file2 /dir/` | Move multiple files    |
| `mv dir1 /dir2/`       | Move directory         |
| `mv -i file /dir/`     | Ask before overwrite   |
| `mv -f file /dir/`     | Force overwrite        |
| `mv -v file /dir/`     | Show operation details |

