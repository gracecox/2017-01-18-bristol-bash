### Molecules
In the molecules directory, you have a shell script called script.sh containing the following commands:
```
head $2 $1
tail $3 $1
```
While you are in the molecules directory, you type the following command:
```
bash script.sh '*.pdb' -1 -1
```
Which of the following outputs would you expect to see?
```
1. All of the lines between the first and the last lines of each file ending in *.pdb
   in the molecules directory
2. The first and the last line of each file ending in *.pdb in the molecules directory
3. The first and the last line of each file in the molecules directory
4. An error because of the quotes around *.pdb
```
### Species
Leah has several hundred data files, each of which is formatted like this:
```
2013-11-05,deer,5
2013-11-05,rabbit,22
2013-11-05,raccoon,7
2013-11-06,rabbit,19
2013-11-06,deer,2
2013-11-06,fox,1
2013-11-07,rabbit,18
2013-11-07,bear,1
```
Write a shell script called species.sh that takes any number of filenames as command-line parameters, and uses cut, sort, and uniq to print a list of the unique species appearing in each of those files separately.

### Command-line arithmetic
Write a command-line program that does addition and subtraction:
```
$ python arith.py add 1 2
3
$ python arith.py subtract 3 4
-1
```
### Checking files
Write a program called check.py that takes the names of one or more inflammation data files as arguments and checks that all the files have the same number of rows and columns. What is the best way to test your program?

