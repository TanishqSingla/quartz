---
tags:
  - Linux
---
![[f02002.png]]

Here are the most important subdirectories in root
- `/bin` 
	- Contains ready to run programs (executables), including most of the basic Unix commands such as `ls` and `cp`.
	- Most programs are binary programs created by a C programmer and some are shell scripts.
- `/dev` 
	- Contains device files.
- `/etc`
	- This core system configuration directory contains the user password, boot, device, networking and other setup files
- `/home` 
	- Holds home (personal) directories for regular users.
- `/lib`
	- An abbreviation for library.
	- This directory holds library files containing code that executables can use.
	- There are 2 types of libraries
		1. static
		2. shared
- `/proc`
	- Provides system statistics through a browsable directory-and-file interface.
	- Much of the `/proc` subdirectory structure on Linux is unique but many other Unix variants have similar features.
	- The `/proc` directory contains information about currently running processes as well as some kernel parameters.
- `/run`
	- Contains runtime data specific to the systems, including certain process IDs, socket files status records and in many cases system logging.
- `/sys`
	- This directory is similar to `/proc` in that it provides a device and system interface.
- `/sbin` 
	- This directory contains system binaries which can only be run by root user.
- `/tmp` 
	-  A storage area for smaller, temporary files.
	- Any user may read or write from `/tmp`, but the user may not have permission to access another user's files there.
- [[usr Directory|/usr]]
	- Although pronounced as user this directory has no user files.
	- It contains large directory hierarchy, including the bulk of Linux system.
- `/var`
	- The variable subdirectory, where program record information that can change over the course of time. 
	- System logging, user tracking, caches, and other files that system programs create and manage.

### Some other directories
- `/boot` 
	- Contains kernel boot loader files.
	- These files pertain only to verify first stage of Linux startup procedure.
- `/media` 
	- A base attachment point for removable media such as flash drives that is found in many distributions.
- `/opt` 
	- This may contain additional third-party software. Many systems don't use `/opt`