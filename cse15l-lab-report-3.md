# Lab Report 3 - Researching Commands
Arushi Munjal, Lab B03

---

I chose the ***find*** command, which is used for searching a folder hierarchy for filenames that meet a desired criteria. Here are four interesting command-line options for ***find***:

1. **-type** : searches for files by their type. [Source](https://unix.stackexchange.com/questions/483871/how-to-find-files-by-file-type).

```
find technical/ -type f -name "*.txt" 
```

> This command searches for all files in the technical directory that have a `.txt` extension.

```
find technical/ -type d -name "*_files" 
```

> This command searches for all directories in the technical directory whose name ends with `_files`.

2. **-mtime** :  searches for files based on their modification time: [Source](https://www.computerhope.com/unix/ufind.htm).

```
find technical/ -mtime -8
```

> This command searches for all files in the technical directory that were modified within the last 8 days.

```
find technical/ -mtime +10 -mtime -15
```

> This command searches for all files in the technical directory that were modified between 10 and 15 days ago.

3. **-user** name/ **-group** name : **-user** searches for files and directories owned by username or ID 'name'. **-group** searches for files and directories that belong to a particular group. [Source](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).

```
find technical/ -user arushi
```

> This command searches for all files and directories in the technical directory that are owned by the user `arushi`.

```
find technical/ -group user -name "*.jpg"
```

> This command searches for all files in the technical directory that have a .jpg extension and are owned by the group `users`.


4. **-printf**: . Source: 

```
find technical/ -type f -printf "%p\t%u\t%g\t%s\n"
```

> This command searches for all files in the technical/ directory and its subdirectories, and prints their filename, owner, group, and size in a tab-separated format. The -printf option allows for customized output formatting.

```
find technical/ -printf idk
```

> This command searches for idk




