A symbolic link is a file that points to another file or a directory, effectively creating an alias or a shortcut.

To create a symbolic link
```sh
ln -s target linkname
```
`linkname` is the argument for the command that sets the name of the symbolic link.

### Note
Don't forget the `-s` option as it creates a soft link, if it is absent then a hard link wil be creating, giving an additional filename to a single file.