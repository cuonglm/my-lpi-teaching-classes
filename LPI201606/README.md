# Question 1

Why and how to fix this pipe output only one line with en_US.utf8 locale in GNU/Linux:

```sh
$ printf '%b\n' '\U2460' '\U2461' | sort -u
①
```

# Question 2

What is the difference between two commands:

```sh
ls /dev/null /dev/do-not-exist 2>&1 >/dev/null
```

and:

```sh
ls /dev/null /dev/do-not-exist >/dev/null 2>&1
```

# Question 3

What is signals? Which signals can not be caught by process?

# Question 4

With text file in `data.txt`:

 - Which command will change modification time of `data.txt` to some day in the past
 - Print all even lines in `data.txt` to a file named `event_lines.txt`
 - Make in-place change: `Linux` to `LINUX`

`data.txt` content refer from [here](https://en.wikipedia.org/wiki/Linux_distribution)
