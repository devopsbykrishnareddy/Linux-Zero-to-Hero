## The grep command in Linux is used to search for specific text patterns in files or output. It’s extremely powerful for filtering data.

## Basic Usage
grep "pattern" filename

### Example:
grep "error" logfile.txt

👉 Finds and displays all lines containing the word error in logfile.txt.

## Common Options

### 1. Ignore Case
grep -i "error" logfile.txt

👉 Matches Error, ERROR, error, etc.

### 2.Show Line Numbers
grep -n "error" logfile.txt

👉 Displays line numbers along with matching lines.

### 3. Search Recursively
grep -r "error" /var/log/

👉 Searches in all files under /var/log/ recursively.

### 4.Count Matches
grep -c "error" logfile.txt


## Examples

#/etc/passwd => i want to search work in this path
use grep word and from which path
grep root /etc/passwd

### to print numbers  use "-n"
grep -n root /etc/passwd

### we can find multiple words from single file , here in example words are "root" and "student"

grep -e root -e student /etc/passwd

### We can able to find single word from two different files

grep root /etc/passwd /etc/group

### to print 4 lines before Krishna word
grep -nB4 krishna /etc/group

### print 4 lines after Krishna word
grep -nA4 krishna /etc/group


