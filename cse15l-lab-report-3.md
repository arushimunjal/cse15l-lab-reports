# Lab Report 3 - Researching Commands
Arushi Munjal, Lab B03

---

I choose the find command, which is used for searching a folder hierarchy for filenames that meet a desired criteria. Here are four interesting command-line options for find:

1. **-type** : searches for files by their type. 

```
find technical/ -type f -name "*.txt" 
```

> This command searches for all regular files in the technical directory that have a .txt extension.

```
find technical/ -type d -name "*_files" 
```

> This command searches for all directories in the technical directory whose name ends with _files.

2. **mtime** :  searches for files based on their modification time.

```
find technical/ -mtime -7
```

> This command searches for all files in the technical directory that were modified within the last 7 days.

```
find technical/ -mtime +30 -mtime -90
```

> This command searches for all files in the technical directory that were modified between 30 and 90 days ago.

3. **-user / -group**: 

```
find technical/ -user john
```

> This command searches for all files and directories in the technical/ directory that are owned by the user john.

```
find technical/ -group developers -name "*.py"
```

> This command searches for all files in the technical/ directory that have a .py extension and are owned by the group developers.


4. **-printf*: 

```
find technical/ -type f -printf "%p\t%u\t%g\t%s\n"
```

> This command searches for all files in the technical/ directory and its subdirectories, and prints their filename, owner, group, and size in a tab-separated format. The -printf option allows for customized output formatting.

```
find technical/ -printf idk
```

> This command searches for idk




