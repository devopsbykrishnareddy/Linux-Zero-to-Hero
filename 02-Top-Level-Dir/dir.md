### In Linux, the top-level directory is called the root directory and is represented by a single forward slash:
/

Everything in Linux is organized under this root directory. Unlike Windows (which has multiple drives like C:\, D:\), Linux has **one unified directory tree that starts from /.

### Top-Level Directories in Linux (under /)

Here are the most common ones you’ll see when you run ls /:

| Directory | Purpose                                                            |
| --------- | ------------------------------------------------------------------ |
| `/bin`    | Essential user binaries (commands like `ls`, `cp`, `mv`).          |
| `/sbin`   | System binaries (for system admin tasks, e.g., `mount`, `reboot`). |
| `/boot`   | Boot loader files (kernel, initrd).                                |
| `/dev`    | Device files (e.g., `/dev/sda` for disks, `/dev/null`).            |
| `/etc`    | System configuration files (like network, users, services).        |
| `/home`   | User home directories (`/home/username`).                          |
| `/lib`    | Shared libraries needed by system programs.                        |
| `/media`  | Mount points for removable media (USB, CDs).                       |
| `/mnt`    | Temporary mount point for filesystems.                             |
| `/opt`    | Optional/add-on software.                                          |
| `/proc`   | Virtual filesystem for process info (e.g., `/proc/cpuinfo`).       |
| `/root`   | Home directory for the root (admin) user.                          |
| `/run`    | Runtime data (like process IDs, sockets).                          |
| `/srv`    | Data for services (like web or FTP servers).                       |
| `/sys`    | Virtual filesystem with device/system info.                        |
| `/tmp`    | Temporary files (cleared on reboot).                               |
| `/usr`    | User programs, libraries, docs (most software lives here).         |
| `/var`    | Variable data (logs, spool, caches).                               |

In summary:

/ is the top-level directory (root).

All other directories are subdirectories under /.

This structure follows the FHS (Filesystem Hierarchy Standard).