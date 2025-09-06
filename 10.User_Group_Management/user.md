## 1. Check Current User
whoami

## 2. Show Logged-in Users
who

👉 Shows all users currently logged in.

## 3. Add a New User
sudo adduser krishna

or

sudo useradd krishna


👉 Creates a new user named krishna.
(adduser is more friendly, useradd is low-level.)


## 4. Set/Change User Password
passwd krishna

👉 Sets or changes password for user krishna.

## 5. Switch User
su - krishna


## 6. Check User Identity
id

👉 Shows your user ID (UID), group ID (GID), and groups.

## 7. List All Users
cat /etc/passwd


## 8. Delete a User
sudo deluser krishna

or

sudo userdel krishna


👉 Removes a user account.

| Command                      | Purpose                     |
| ---------------------------- | --------------------------- |
| `whoami`                     | Show current user           |
| `who` / `w`                  | Show logged-in users        |
| `adduser <name>`             | Create new user             |
| `passwd <name>`              | Set/change password         |
| `su - <user>`                | Switch user                 |
| `id`                         | Show UID, GID, groups       |
| `cat /etc/passwd`            | List all users              |
| `deluser <name>`             | Delete user                 |
| `last`                       | Show login history          |


