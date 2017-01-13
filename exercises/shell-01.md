## Many ways to do the same thing - absolute vs relative paths
For a hypothetical filesystem location of /Users/amanda/data/, select each of the below commands that Amanda could use to navigate to her home directory, which is Users/amanda.
```
1. cd .
2. cd /
3. cd /home/amanda
4. cd ../..
5. cd ~
6. cd home
7. cd ~/data/..
8. cd
9. cd ..
```
##Relative path resolution
Using the filesystem diagram below, if pwd displays /Users/thing, what will ls ../backup display?

![image for challenge](https://github.com/swcarpentry/shell-novice/blob/gh-pages/fig/filesystem-challenge.svg)

```
1. ../backup: No such file or directory
2. 2012-12-01 2013-01-08 2013-01-27
3. 2012-12-01/ 2013-01-08/ 2013-01-27/
4. original pnas_final pnas_sub
```
##Listing
Assuming a directory structure as in the previous exercise, if pwd displays /Users/backup, and -r tells ls to display things in reverse order, what command will display:
```
pnas_sub/ pnas_final/ original/
```
```
1. ls pwd
2. ls -r -F
3. ls -r -F /Users/backup
4. Either #2 or #3 above, but not #1
```

##Renaming files
Suppose that you created a .txt file in your current directory to contain a list of the statistical tests you will need to do to analyze your data, and named it: statstics.txt

After creating and saving this file you realise the filename is wrong! You want to correct the mistake, which of the following commands could you use to do so?
```
1. cp statstics.txt statistics.txt
2. mv statstics.txt statistics.txt
3. mv statstics.txt .
4. cp statstics.txt .
```
##Moving and Copying
What is the output of the closing ls command in the sequence shown below?
```
$ pwd
/Users/jamie/data
$ ls
proteins.dat
$ mkdir recombine
$ mv proteins.dat recombine
$ cp recombine/proteins.dat ../proteins-saved.dat
$ ls
```
```
1. proteins-saved.dat recombine
2. recombine
3. proteins.dat recombine
4. proteins-saved.dat
```
##Organizing Directories and Files
Jamie is working on a project and she sees that her files aren’t very well organized:
```
$ ls -F
analysed/  fructose.dat    raw/   sucrose.dat
```
The fructose.dat and sucrose.dat files contain output from her data analysis. What command(s) covered in this lesson does she need to run so that the commands below will produce the output shown?
```
$ ls -F
analysed/   raw/
$ ls analysed
fructose.dat    sucrose.dat
```
