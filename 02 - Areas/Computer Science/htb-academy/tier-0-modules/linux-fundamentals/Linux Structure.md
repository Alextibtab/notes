---
module_tier: 0
module_name: [[Linux Fundamentals Module]]
platform: HTB
---
# Linux Structure
---
## History
At first, Linux was a personal project started in 1991 by a Finnish student named Linus Torvalds. His goal was to create a new, free operating system kernel. Over the years Linux kernel has gone form a small number of files written in C under licensing that prohibited commercial distribution to the latest version with over 23 million lines of source code licensed under the GNU General Public License v2.

Linux is available in over 600 distributions based on the Linux kernel. Linux is generally considered more secure than other operating systems. Since Linux is free and open-source, the source code can be modified and distributed commercially or non-commercially by anyone. Linux-based operating systems run on servers, mainframes, desktops, embedded systems such as routers, televisions, video game consoles and more.

## Philosophy
---
| Principle                                                     | Description                                                                                                                                                     |
| ------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Everything is a file`                                        | All configuration files for the various services running on the Linux operating system are stored in one or more text files.                                    |
| `Small, single-purpose programs`                              | Linux offers many different tools that we will work with, which can be combined to work together                                                                |
| `Ability to chain programs together to perform complex tasks` | The integration and combination of different tools enables us to carry out many large and complex tasks, such as processing or filtering specific data results. |
| `Avoid captive user interfaces`                               | Linux is designed to work mainly with the shell which gives the user greater control over the operating system                                                  |
| `Configuration data stored in a text file`                    | An example of such a file is the `/etc/passwd` file, which stores all users registered on the system.                                                                                                                  | 

## Components
---
| Component         | Description                                                                                                                                                                                                                                                                                                                                   |
| ----------------- | --------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Bootloader`      | A piece of code that runs to guide the bootleg process to start the operating system. Parrot uses the GRUB bootloader.                                                                                                                                                                                                                        |
| `OS Kernel`       | The kernel is the main component of an operating system. It manages the resources for system's I/O devices at the hardware level.                                                                                                                                                                                                             |
| `Daemons`         | Background services are called "daemons" in Linux. Their purpose is to ensure that key functions such as scheduling, printing and multimedia are working correctly. These small programs load after the computer is booted.                                                                                                                   |
| `OS Shell`        | The operating system shell or the command language interpreter.                                                                                                                                                                                                                                                                               |
| `Graphics Server` | This provides a graphical sub-system (server) called "X" or "X-server" that allows graphical programs to run locally or remotely on an X-windowing system.                                                                                                                                                                                    |
| `Window Manager`  | Also known as a graphical user interface (GUI). There are many options including GNOME, KDE, MATE, Unity and Cinnamon. A desktop environment usually has several applications, including file and web browsers. These allow the user to access and manage the essential and frequently accessed features and services of an operating system. |
| `Utilities`       | Applications or utilities are programs that perform particular functions for the user or another program.                                                                                                                                                                                                                                     | 
## Linux Architecture
---
| Layer            | Description                                                                                                                                                                                                                                                                                        |
| ---------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `Hardware`       | Peripheral devices such as the system's RAM, hard drive, CPU and others                                                                                                                                                                                                                            |
| `Kernel`         | The core of the Linux operating system, whose function is to virtualize and control common computer hardware resources like CPU, allocated memory, accessed data, and others. The kernel gives each process its own virtual resources and prevents/mitigates conflicts between different processes |
| `Shell`          | A command-line interface (CLI), also known as a shell that a user can enter commands into to execute the kernels functions.                                                                                                                                                                        |
| `System Utility` | Makes available to the user all of the system's functionality.                                                                                                                                                                                                                                     | 

## File System Hierarchy
---
![[linuxFileStructure.png]]

| Path     | Description                                                                                                                                                                                                                                                                                                                      |
| -------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `/`      | The top-level directory is the root filesystem and contains all of the files required to boot the operating system before other filesystems are mounted as well as the files required to boot the other filesystems. After boot, all of the other filesystems are mounted at standard mount points as subdirectories of the root |
| `/bin`   | Contains essential command binaries                                                                                                                                                                                                                                                                                              |
| `/boot`  | Consists of the static bootloader, kernel executable, and files required to boot the Linux OS.                                                                                                                                                                                                                                   |
| `/dev`   | Contains device files to facilitate access to every hardware device attached to the system                                                                                                                                                                                                                                       |
| `/etc`   | Local system configuration files. Configuration files for installed applications may be saved here as well                                                                                                                                                                                                                       |
| `/home`  | Each user on the system has a subdirectory here for storage.                                                                                                                                                                                                                                                                     |
| `/lib`   | Shared library files that are required for system boot.                                                                                                                                                                                                                                                                          |
| `/media` | External removable media devices such as USB drives are mounted here                                                                                                                                                                                                                                                             |
| `/mnt`   | Temporary mount points for regular filesystems                                                                                                                                                                                                                                                                                   |
| `/opt`   | Optional files such as third-party tools can be saved here                                                                                                                                                                                                                                                                       |
| `/root`  | The home directory for the root user                                                                                                                                                                                                                                                                                             |
| `/sbin`  | This directory contains executables used for system-administration.                                                                                                                                                                                                                                                              |
| `/tmp`   | The operating system and many programs use this directory to store temporary files. This directory is generally cleared upon system-boot and may be deleted at other times without any warning.                                                                                                                                  |
| `/usr`   | Contains executables, libraries, man files, etc.                                                                                                                                                                                                                                                                                 |
| `/var`   | This directory contains variable data files such as log files etc.                                                                                                                                                                                                                                                               | 

up: [[Linux Fundamentals Module]]
tags: #HTB #Tier_0 #Linux_Fundamentals 