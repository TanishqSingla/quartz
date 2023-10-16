- Unlike [[gzip]], tar can pack multiple files and directories into a single file called [[Archives|archive]]. 

**To create an archive**
```sh
tar cvf archive.tar file1 file2
```

Archives created by tar have `.tar` suffix.

**Unpacking .tar files**
```sh
tar xvf archive.tar
```

## Table of contents mode
It is generally a good idea to check the contents of the file before extracting it. This can be achieved by using `-t` option.

`-t` option verifies integrity and prints the names of all files inside.