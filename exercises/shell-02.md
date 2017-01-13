## Pipes 1

In our current directory, we want to find the 3 files which have the least number of lines. Which command listed below would work?
```
1. wc -l * > sort -n > head -3
2. wc -l * | sort -n | head 1-3
3. wc -l * | head -3 | sort -n
4. wc -l * | sort -n | head -3
```

## Pipes 2

A file called animals.txt contains the following data:
```
2012-11-05,deer
2012-11-05,rabbit
2012-11-05,raccoon
2012-11-06,rabbit
2012-11-06,deer
2012-11-06,fox
2012-11-07,rabbit
2012-11-07,bear
```
What text passes through each of the pipes and the final redirect in the pipeline below?
```
cat animals.txt | head -5 | tail -3 | sort -r > final.txt
```

## Pipes 3

The command:
```
$ cut -d , -f 2 animals.txt
```
produces the following output:
```
deer
rabbit
raccoon
rabbit
deer
fox
rabbit
bear
```
The command uniq prints only those lines that are not repeated in the input (unique lines). How could the cut and uniq commands be used to find out what animals the file contains (without any duplicates in their names)?

## Loops 1
Suppose that ls initially displays:
```
fructose.dat    glucose.dat   sucrose.dat
```
What is the output of:
```
for datafile in *.dat
do
    ls *.dat
done
```
Now, what is the output of:
```
for datafile in *.dat
do
  ls $datafile
done
```
Why do these two loops give you different outputs?

## Loops 2

In the same directory, what is the effect of this loop?
```
for sugar in *.dat
do
    echo $sugar
    cat $sugar > xylose.dat
done
```
```
1. Prints fructose.dat, glucose.dat, and sucrose.dat,
   and the text from sucrose.dat will be saved to a file called xylose.dat.
2. Prints fructose.dat, glucose.dat, and sucrose.dat,
   and the text from all three files would be concatenated and saved to a file called xylose.dat.
3. Prints fructose.dat, glucose.dat, sucrose.dat, and xylose.dat,
   and the text from sucrose.dat will be saved to a file called xylose.dat.
4. None of the above.
```

## Loops 3
In another directory, where ls returns:
```
fructose.dat    glucose.dat   sucrose.dat   maltose.txt
```
What would be the output of the following loop?
```
for datafile in *.dat
do
    cat $datafile >> sugar.dat
done
```
```
1. All of the text from fructose.dat, glucose.dat and sucrose.dat would be concatenated
   and saved to a file called sugar.dat.
2. The text from sucrose.dat will be saved to a file called sugar.dat.
3. All of the text from fructose.dat, glucose.dat, sucrose.dat and maltose.txt would be
   concatenated and saved to a file called sugar.dat.
4. All of the text from fructose.dat, glucose.dat and sucrose.dat would be printed
   to the screen and saved to a file called sugar.dat
```

### grep
```
The Tao that is seen
Is not the true Tao, until
You bring fresh toner.

With searching comes loss
and the presence of absence:
"My Thesis" not found.

Yesterday it worked
Today it is not working
Software is like that.
```
From the above text, contained in the file haiku.txt, which command would result in the following output:
```
and the presence of absence:
```
```
1. grep "of" haiku.txt
2. grep -E "of" haiku.txt
3. grep -w "of" haiku.txt
4. grep -i "of" haiku.txt
```

## Loops 4

The expr does simple arithmetic using command-line parameters:
```
$ expr 3 + 5
8
$ expr 30 / 5 - 2
4
```
Given this, what is the output of:
```
for left in 2 3
do
    for right in $left
    do
        expr $left + $right
    done
done
```

