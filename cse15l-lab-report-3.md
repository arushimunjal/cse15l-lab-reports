# Lab Report 3 - Researching Commands
Arushi Munjal, Lab B03

---
I chose the ***find*** command, which is used for searching files and directories in a file system that meet a desired criteria. Here are four interesting command-line options for ***find***:

1. **-type** : filters the search results based on the type of file or directory specificed by the command. `-type f` matches only regular files. `-type d` matches only directories. `-type l` matches only symbolic links. - [source](https://ss64.com/bash/find.html).

```
find ./technical -type f -name "*.txt" 
```
Output:

![Image](ex1.1.png)

> This command searches for all files in the technical directory that have a `.txt` extension. This command is useful for quickly locating all text *files* and perform further manipulation. It can help you understand the structure of the project or any gaps. The output shows that there are several `.txt` files in the docsearch directory.

```
find ./technical -type d -name "*_files" 
```
Output:

![Image](ex1.2.png)

> This command searches for all directories in the technical directory whose name ends with `_files`. This command is useful for locating all *directories* in the technical directory that have a specific names in the file system. The output shows that there are no directories in docsearch that have an extension of _files.


2. **-mtime** :  searches for files based on their modification time. `-mtime +N` find the files that were last modified more than N days ago. `-mtime -N` find the files that were last modified less than N days ago. `-mtime N` find files that were last modified exactly N days ago - [source](https://www.computerhope.com/unix/ufind.htm).


```
find ./technical -mtime -7
```

Output:
![Image](ex2.1.png)

> This command searches for all files in the technical directory that were modified within the last 7 days. This command is useful for searching for altered files/directories from the previous week. The output shows that most files were edited in the past week.

```
find ./technical -mtime +10 -mtime -15
```

Output:
![Image](ex2.2.png)

> This command searches for all files in the technical directory that were modified between 10 and 15 days ago. This command is useful for finding files and directories that were modified within a certain range of time. The output shows that there are no files that were modified within this range. This is because the repo was recently forked, but this command would be helpful in other cases that have an olde4r directory.


3. **-name* "word" : **-name** searches for files and directories that contain the word "word" in the file - [source](https://www.geeksforgeeks.org/find-command-in-linux-with-examples/).

```
find ./technical -name "biomed"
```

Output:
![Image](ex3.1.png)

> This command searches for all files and directories in the technical directory that contain the word "biomed". In. this case, this command is useful for locating the subdirectory of /technical that relate to `biomed`. The output shows that there is 1 directory that contains the word `biomed`.

```
find ./technical -name "*s"
```

Output:
![Image](ex3.2.png)

> This command searches for all files in the technical directory that end in "s" inside the ./technical directory (* searches for the end specifically). The command in this case can be useful for finding specific names, such as plural (shown in the output). You can also search files that end in numbers or special characters to make it easier to find unique files.

4. **-delete** : deletes the files and directories that you specify after the command - [source](https://www.computerhope.com/unix/ufind.htm).

```
find ./technical -name "*s" -type f -delete
```

Output:
![Image](ex4.1.png)

> This command searches for all files (using `-type f` option) in the technical directory that end with the "s" (using `-name "*.s` option), and then deletes them using the `-delete` option. This command is useful for automating the processes of deleting a certain set of files. The output shows that if we use the command `find ./technical -name "*s"` from example 3, there are 2 files that correlate to this search: ./technical/government/Alcohol-Problems and ./technical/plos. After using this command to delete those files, we can use the command from example 3 once again, which shows that those files do not exist anymore.

```
find ./technical -type f -name "*.txt" -delete
```

Output:
![Image](ex4.2.png)

> This command searches for all files in the technical directory that have a `.txt` extension. and then deletes them using the `-delete` option. This command can be useful to remove all files and directories that are a certain type. The output shows that if we use the command `find ./technical -type f -name "*.txt" ` from example 1, there are several, if not all, files that correlate to this search. After using this command to delete those files, we can use the command from example 1 once again, which shows that those files do not exist anymore.
