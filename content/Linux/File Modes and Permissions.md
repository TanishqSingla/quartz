---
tags:
  - Linux
---

![[f02001.png]]

- `r` means file is readable
- `w` means file is writable
- `x` means file is executable
- `-` is a placeholder for permissions that hasn't been granted

Some executable files have an `s` in the user permissions listing instead of an x., This indicates that the executable is`setuid`, meaning that when the program is executed the file runs as though the file owner is the user instead of you.
