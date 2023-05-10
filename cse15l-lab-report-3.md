# Lab Report 3 - Researching Commands
Arushi Munjal, Lab B03

---
I chose the ***find*** command, which is used for searching files and direcotries in a file system that meet a desired criteria. Here are four interesting command-line options for ***find***:

1. **-type** : filters the search results based on the type of file or directory specificed by the command. `-type f` matches only regular files. `-type d` matches only directories. `-type l` matches only symbolic links. - [source](https://ss64.com/bash/find.html).


```
find technical/ -type f -name "*.txt" 
```

> This command searches for all files in the technical directory that have a `.txt` extension. This command is useful for quickly locating all text *files* and perform further manipulation. It can help you understand the structure of the project or any gaps.

```
find technical/ -type d -name "*_files" 
```

> This command searches for all directories in the technical directory whose name ends with `_files`. This command is useful for locating all *directories* in the technical directory that have a specific names in the file system.


2. **-mtime** :  searches for files based on their modification time. `-mtime +N` find the files that were last modified more than N days ago. `-mtime -N` find the files that were last modified less than N days ago. `-mtime N` find files that were last modified exactly N days ago - [source](https://www.computerhope.com/unix/ufind.htm).


```
find technical/ -mtime -7
```

> This command searches for all files in the technical directory that were modified within the last 7 days. This command is useful for searching for altered files/directories from the previous week.

```
find technical/ -mtime +10 -mtime -15
```

> This command searches for all files in the technical directory that were modified between 10 and 15 days ago. This command is useful for finding files and directories that were modified within a certain range of time.

3. **-user** name / **-group** name : **-user** searches for files and directories owned by username or ID 'name'. **-group** searches for files and directories that belong to a particular group - [source](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).

```
find technical/ -user arushi
```

> This command searches for all files and directories in the technical directory that are owned by the user `arushi`. This command is useful for locating all files and directories that are owners my a certain user and track that user's progress. 

```
find technical/ -group user -name "*.jpg"
```

> This command searches for all files in the technical directory that have a .jpg extension and are owned by the group `users`. This command is useful for finding all files of a certain set that are owned by a specific group, such as if a group quits/finishes the project.


4. **-delete** : deletes the files and directories that you specify after the command - [source](https://www.computerhope.com/unix/ufind.htm).

```
find /technical -type f -name "*.txt" -delete
```

> This command searches for all files (using `-type f` option) in the technical directory that end with the .txt extension (using `-name "*.txt` option), and then deletes them using the `-delete` option. This command is useful for automating the processes of deleting a certain set of files. 

```
find /technical -user tanisha -delete
```

> This command searches for all files and directories in the technical directory and its subdirectories that are owned by user tanisha using the `-user tanisha` option, and then deletes them using the `-delete` option. This command can be useful to remove all files and directories owned by a specific user. To only delete empty files, type `find /technical -type d -user tanisha -empty -delete ` instead.
