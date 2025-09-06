The cal command in Linux is used to display a calendar in the terminal. It’s simple but very handy.

# 1.Cal command

## Basic Usage
cal
👉 Shows the current month’s calendar.

## Show a specific month/year
cal 12 2025


## show entire year

cal -y

Number of months

Show previous, current, and next month:

cal -3

## Julian calendar (day numbers of the year)

cal -j

## 2.The pwd command in Linux stands for Print Working Directory.
It simply shows the absolute path of your current working directory in the terminal.

## Basic command

pwd

👉 Prints your current directory.

Example:

/home/krishna/Documents

Options

-L (Logical) [default]

Shows the path as stored in your environment, including symlinks.

pwd -L

## 3.The whoami command in Linux is very simple — it tells you the username of the currently logged-in user.

whoami

## Example:

krishna

👉 Here, krishna is the logged-in user.

## When to use

To quickly confirm which user you are logged in as (especially useful after switching users with su or sudo su).

To check your identity on shared systems or servers.

## Related Commands

who → shows all logged-in users.

id → shows user ID (UID), group ID (GID), and group memberships.

id
uid=1000(krishna) gid=1000(krishna) groups=1000(krishna),27(sudo)


echo $USER → also prints current username (from environment variable).

## 4.The date command in Linux is used to display or set the system date and time.

date

## Example Output:

Fri Sep  5 07:52:31 IST 2025

Custom Format

You can format the output using + and format specifiers.

## Common examples:

date +"%Y-%m-%d"        # 2025-09-05   (YYYY-MM-DD)
date +"%d/%m/%Y"        # 05/09/2025   (DD/MM/YYYY)
date +"%A"              # Friday       (Full weekday name)
date +"%H:%M:%S"        # 07:52:31     (24-hour time)
date +"%I:%M %p"        # 07:52 AM     (12-hour time)

Show Past/Future Dates
date --date="yesterday"
date --date="next Friday"
date --date="2 days ago"
date --date="10 weeks"

## Setting Date & Time (root required)
sudo date -s "2025-09-05 08:00:00"

## 5.The ls command in Linux is used to list files and directories in the current directory (or a specified one). It has many useful options.

ls
👉 Lists files in the current directory.

## Show in Long Format
ls -l
👉 Displays detailed info: permissions, owner, group, size, date.

Example:
-rw-r--r--  1 krishna users   1234 Sep  5 07:40 file.txt

## Show Hidden Files
ls -a

👉 Includes hidden files (those starting with . like .bashrc).

## Combine Options
ls -la
👉 Long format and show hidden files.

## Sort by Time
ls -lt

👉 Sorts files by last modified time (latest first).
Add -r for reverse order:

ls -ltr

## Sort by Size
ls -lS

## Show Directories Only

ls -d */

## Recursive Listing
ls -R

## Examples Summary

| Command   | Purpose                      |
| --------- | ---------------------------- |
| `ls`      | List files                   |
| `ls -l`   | Long format (details)        |
| `ls -a`   | Show hidden files            |
| `ls -la`  | Long + hidden                |
| `ls -lh`  | Long + human readable sizes  |
| `ls -ltr` | Sorted by time, oldest first |
| `ls -lS`  | Sorted by size               |
| `ls -R`   | Recursive listing            |
| `ls -F`   | Classify with symbols        |


## 6. how to count number of lines in a file in linux
wc -l file

## 7. How to compare and display different between two files in Linux
diff -u fileA fileB 

## 8. The find command in Linux is a powerful tool to search for files and directories based on different criteria such as name, type, size, modification time, permissions, and more.

## Basic Syntax

find [path] [options] [expression]

path → directory to search (use . for current directory)

options/expression → criteria to match

## Examples
### a.Find a File by Name
find . -name "file.txt"
👉 Searches for file.txt in the current directory and all subdirectories.

Case-insensitive search:
find . -iname "file.txt"

### b.Find Directories by Name
find /home/krishna -type d -name "Documents"

-type d → directories
-type f → files

### c. Find Files by Extension
find . -type f -name "*.txt"
👉 Finds all .txt files in the current directory recursively.

### d. Find Files by Size

find . -size +1M

+1M → files larger than 1 MB

-1M → files smaller than 1 MB

1M → files exactly 1 MB

## 9. commands to check free RAM and memory usage

## a. free Command
Displays memory usage in a simple table.
free -h
-h → human-readable (shows MB/GB instead of bytes)

### Example Output:
              total        used        free      shared  buff/cache   available
Mem:           7.8G        3.2G        1.0G        200M        3.6G        4.1G
Swap:          2.0G        0.0G        2.0G

free → truly free memory

available → memory available for new processes

### b. top Command

Shows a real-time view of system processes and memory usage.

top

Look at KiB Mem or MiB Mem section to see RAM usage.
Press q to exit.

### c. htop Command (interactive, needs installation)

htop

Colored, interactive version of top.

Shows RAM, swap, CPU usage, and running processes.

Install if missing:
sudo apt install htop     # Debian/Ubuntu
sudo yum install htop     # RHEL/CentOS

## 10. commands to check disk utilization

## a. df – Disk Free

Shows disk space usage of filesystems.

df -h

-h → human-readable (GB/MB instead of bytes)
### Example Output:
Filesystem      Size  Used Avail Use% Mounted on
/dev/sda1        50G   20G   28G  42% /
tmpfs           7.8G     0  7.8G   0% /dev/shm

Size → total size of filesystem
Used → space used
Avail → space available
Use% → percentage used
Mounted on → mount point

## b. du – Disk Usage
Shows disk usage of files/directories.

Check size of current directory:

du -sh .


-s → summary (total size)

-h → human-readable

Check all subdirectories:

## c. ls – Show File Sizes

ls -lh

-l → long listing
-h → human-readable
Useful to see individual file sizes in a directory.

## d. df with Specific Filesystem

df -h /home

Checks usage of a specific partition or directory.










