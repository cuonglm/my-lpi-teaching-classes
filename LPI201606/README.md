# Question 1

Why and how to fix this pipe output only one line with en_US.utf8 locale in GNU/Linux:

```sh
$ printf '%b\n' '\U2460' '\U2461' | sort -u
①
del  \n because  \n is down the line symbol ```

# Question 2

What is the difference between two commands:

```sh
ls /dev/null /dev/do-not-exist 2>&1 >/dev/null
```

and:

```sh
ls /dev/null /dev/do-not-exist >/dev/null 2>&1
```
Excute the commands 1, there is a line "No such file or directory' in Desktop
Excute the commands 2, nothing the line in Desktop

because excute command 1, the output was sent into the desktop
excute command 2, the output was sent into the directory "dev/null"  
# Question 3

What is signals? Which signals can not be caught by process?
singnals is the mess sent to process to  control process excute some actions
singnals can't caught by process is SIGKILL and SIGSTOP  

# Question 4

With text file in `data.txt`:

 - Which command will change modification time of `data.txt` to some day in the past
used 'touch -t [yyyyMMddhhmm]' 
exam 
touch -t 201608011800 data.txt :  change modification time of data.txt to 01/08/2016 18:00 

 - Print all even lines in `data.txt` to a file named `event_lines.tx`
  sed '1d;n;d' data.txt >> event_lines.tx
 - Make in-place change: `Linux` to `LINUX`

`data.txt` content refer from [here](https://en.wikipedia.org/wiki/Linux_distribution)
    sed -i -e 's/Linux/LINUX' data.txt
  
