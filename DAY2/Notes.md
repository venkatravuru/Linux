# Day 2: Introduction to Linux  

## 1. What is Linux?  
Linux is an **open-source operating system** based on Unix, widely used for servers, cloud computing, and embedded systems.

### Key Features:  
✔ **Operating System:** Manages hardware and software resources.  
✔ **Open Source:** Free to use, modify, and distribute.  
✔ **Developed in 1991** by **Linus Torvalds**.  
✔ **Multi-User & Multi-Tasking:** Supports multiple users and processes simultaneously.  
✔ **Case Sensitive:** Treats uppercase and lowercase differently (`File.txt` ≠ `file.txt`).

---

## 2. Linux Distributions (Flavors)  
A **distribution (distro)** is a customized version of Linux that includes the OS, package management, and additional tools.

| **Distro**   | **Use Case**                                      |
|-------------|--------------------------------------------------|
| **RedHat**  | Enterprise-grade, commercial support (RHEL)      |
| **Ubuntu**  | User-friendly, widely used for desktops/servers  |
| **CentOS**  | Community-supported version of RedHat           |
| **Debian**  | Stable, known for reliability                   |
| **SUSE Linux** | Enterprise use, strong in SAP environments  |

Other distros: Fedora, Arch Linux, Kali Linux (for penetration testing), etc.

---

## 3. Linux Directory Structure  
Linux follows a hierarchical directory structure where everything starts from **`/` (root directory)**.


## 📌 Linux File System Diagram
![Linux Directory Structure](https://media.geeksforgeeks.org/wp-content/uploads/20210501124411/dir.png)




### **Key Directories Explained**
- **`/` (Root Directory):** The top-most directory that contains all files and subdirectories.  
- **`/bin`** - Essential binary executables (commands) like `ls`, `cp`, `mv`.  
- **`/sbin`** - System binaries used for system administration (e.g., `reboot`, `fdisk`).  
- **`/etc`** - System and application configuration files (e.g., `/etc/passwd` for user details).  
- **`/home`** - User home directories (`/home/user1`, `/home/user2`). Each user stores personal files here.  
- **`/dev`** - Represents hardware devices as files (e.g., `/dev/sda` for hard drives).  
- **`/root`** - Home directory for the **root (admin)** user.  
- **`/opt`** - Optional software packages installed manually.  
- **`/lib`** - Shared libraries required by system binaries (`/bin`, `/sbin`).  
- **`/proc`** - A virtual filesystem that provides system information (`/proc/cpuinfo`).  
- **`/tmp`** - Temporary file storage, often cleared on reboot.  

---

This content will help students understand Linux fundamentals before moving to hands-on practice. 🚀



