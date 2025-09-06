In Linux, file permissions control who can read, write, or execute a file or directory. They are fundamental to security and proper functioning of the system.

## 1. Permission Types

Each file/directory has 3 types of permissions:

r (read) → View file contents / list directory

w (write) → Modify file / create or delete files in directory

x (execute) → Run file as program / access directory contents

## 2. Permission Groups

Permissions are assigned to three categories of users:

Owner (u) → The user who owns the file

Group (g) → Users in the file’s group

Others (o) → Everyone else

## 3. Viewing Permissions

Use ls -l to see file permissions:

ls -l
-rwxr-xr--  1 user group  1234 Sep  5  test.sh

Breakdown:

- → file type (- = file, d = directory, l = link)

rwx → Owner permissions (read, write, execute)

r-x → Group permissions (read, execute)

r-- → Others permissions (read only)

## 4. Changing Permissions

Use chmod (change mode):

Symbolic mode:

chmod u+x file.sh     # Add execute for owner
chmod g-w file.sh     # Remove write for group
chmod o=r file.sh     # Set others to read only

Numeric (octal) mode:

r = 4, w = 2, x = 1

Add values together.

7 = rwx, 6 = rw-, 5 = r-x, 4 = r--

Example:

chmod 755 file.sh     # rwx for owner, r-x for group, r-x for others
chmod 644 file.txt    # rw- for owner, r-- for group, r-- for others

## 5. Changing Ownership

Change owner:

chown user file.txt


Change group:

chgrp developers file.txt


Change both:

chown user:group file.txt

## 6. Special Permissions

Sticky Bit (t) → On directories, only file owner can delete files.

chmod +t /tmp


Setuid (s) → Program runs with owner’s permissions.

Setgid (s) → Files in a directory inherit the group of that directory.