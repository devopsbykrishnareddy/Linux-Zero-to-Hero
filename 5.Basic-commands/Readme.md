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


