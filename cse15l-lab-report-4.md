# Lab Report 4 - Editing with Vim
Arushi Munjal, Lab B03

---

**Step 1: Log into ieng6.**

```
$ ssh cs15lsp23oi@ieng6.ucsd.edu <enter>
(cs15lsp23oi@ieng.ucsd.edu) Password: <paste password> <enter>
```

> To access my log in details, I used `Control + C` and `Control V` on Lab Report 1. These steps allow me to log into my remote ieng6 account.
 
![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/c7b10f25-76b7-423d-aa79-adc303599fe6)

  
**Step 2: Clone your fork of the repository from your Github account.**

```
$ git clone https://github.com/arushimunjal/lab7new
```
> To access the link of the repository, I opened the link from the lab7 instructions and forked it on Github. Then, I cloned it in my terminal by using `git clone`, which clones the lab7 repository into my remote account.

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/cd7d2d90-55a8-461e-91a7-9ce3af31d36e)


**Step 3: Run the tests, demonstrating that they fail.**

```
$ ls
$ cd lab7 <enter>
$ bash t <tab> <enter>
```
 
![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/e0acfa90-f495-4304-a660-6525aa0ee6eb)


> To run the tests, I used `ls` to find the list of files of the repo and `cd` to access and enter lab7. Then, I typed `bash t` and used <tab> to autocomplete `t` to become `test.sh`. `bash` ran the commands in the `test.sh` files.
  
**Step 4: Edit the code file to fix the failing test.**
 
```
$ vim L<tab>.java <enter>
$ /index1 <enter> n n n n n n n n n l l l l l r 2 <esc> :wq
```
 
![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/06b83078-297d-493a-98d7-edf5082dbfad)

![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/1707e604-9d39-4058-8231-69c0d1d62a0f)


> To open the ListExamples java file, I typed `vim` because that is the text editor we need to edit the code file. I typed `L` and then `tab` in order to autocomplete it to `ListExamples`. I typed `.java` and `enter` to open the java code. Then, I typed `/index` which searches for the word `index` in the code. I typed `n` 9 times to find the nineth occurance of `index` in the file and `l` 5 times in order to move around 5 characters to the right. Then, I typed `r` ans `2` which changed `index1` to become `index2`, as `r` replaces a single character and I used it to replace `1` to `2`. Finally, I pressed `esc` to escape vim's insert mode and `:wq` to save the edits.
  
**Step 5: Run the tests, demonstrating that they now succeed.**
 
```
$ bash t <tab> <enter>
```
 
![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/b58577f7-196a-4ce2-83b5-653aa907e1c7)


> To run the tests again after editing the code, I typed `bash t` and <tab> again to autocomplete `t` to `test.sh`.
  
**Step 6: Commit and push the resulting change to your Github account.**
 
```
$ git status
$ git add L<tab>.java <enter>
$ git commit -m Done <enter>
$ git push origin main
$ git status
```
 
![Image](https://github.com/arushimunjal/cse15l-lab-reports/assets/127368251/48f4b8a1-e3af-4383-a84b-4141ce201968)



> I first used `git status` to check the state of the workinng direcotry and the staging area. Then, I used `git add ListExamples.java` to add my change in the local working directory to the repository. I typed `L` and then `tab` to autocomplete `L` to `ListExamples`, and then added `.java`. Then, I used `git commit -m` to commit the staged files and `done` after as my comment that describes the intention of the commit. I typed `git push origin` to finally push/upload the local branch to the repository. Lastly, I typed `git status` once again to check the status of the repo after comminiting the change and to ensure that the git push succeeded.
