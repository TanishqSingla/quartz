---
tags:
  - Linux
  - Bash
---
It is common to see an archive created using [[tar]] is further compressed using [[gzip]].

The file created by this process has `.tar.gz` as suffix.

**To unpack compressed archive**
```
gunzip file.tar.gz
tar xvf file.tar
```
