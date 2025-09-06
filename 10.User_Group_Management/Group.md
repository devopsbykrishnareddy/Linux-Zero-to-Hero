## Group Management in Linux

There are two types of groups:

## Primary Group → each user belongs to exactly one.

## Secondary (Supplementary) Groups → a user can be a member of many.

## 1. View Groups

Show groups for the current user:

groups

Show groups for a specific user:

groups krishna

Show all groups on the system:

Show all groups on the system:

## 2. Create a Group
sudo groupadd developers

👉 Creates a group named developers.

## 3. Delete a Group
sudo groupdel developers

👉 Deletes the developers group.

## 4. Add User to Group
### Add user to a secondary group:
sudo usermod -aG developers krishna

👉 Adds krishna to developers group.
(-aG = append to groups)

Change a user’s primary group:
sudo usermod -g developers krishna

## 5. Remove User from Group
sudo gpasswd -d krishna developers

👉 Removes krishna from developers group.

## 6. Change Group Ownership of a File
chgrp developers project.txt

👉 Assigns project.txt to the developers group.

## 7. Set Default Group for a New User
When creating a user, assign a group:
sudo useradd -g developers john

## 8. Switch Group Temporarily
newgrp developers

👉 Switches current session to developers group.


| Command                      | Purpose                                    |
| ---------------------------- | ------------------------------------------ |
| `groups`                     | Show groups of current user                |
| `groups <user>`              | Show groups of specific user               |
| `getent group`               | List all groups                            |
| `groupadd <name>`            | Create new group                           |
| `groupdel <name>`            | Delete group                               |
| `usermod -aG <group> <user>` | Add user to secondary group                |
| `usermod -g <group> <user>`  | Change user’s primary group                |
| `gpasswd -d <user> <group>`  | Remove user from group                     |
| `chgrp <group> <file>`       | Change group ownership of file             |
| `newgrp <group>`             | Switch to another group in current session |



