# Question 1

Why and how to fix this pipe output only one line with en_US.utf8 locale in GNU/Linux:

```sh
$ printf '%b\n' '\U2460' '\U2461' | sort -u
①
```
$ printf '%b\n' '\U2460' '\U2461' | sort | tr "\n" " "

# Question 2

What is the difference between two commands:

```sh
ls /dev/null /dev/do-not-exist 2>&1 >/dev/null
```
chuyen thong bao loi vao sttout sau do chuyen vao dev null, nen van ghi ra man hinh
and:

```sh
ls /dev/null /dev/do-not-exist >/dev/null 2>&1
```
chuyen thong bao loi vao dev null sau do moi chuyen loi vao sttout nen ko xuat hien loi tren man hinh
# Question 3

What is signals? Which signals can not be caught by process?
sigkill and sigstop
# Question 4

With text file in `data.txt`:

 - Which command will change modification time of `data.txt` to some day in the past
$touch -d "3 day ago" data.txt
 - Print all even lines in `data.txt` to a file named `event_lines.txt`
sed '1d,n,d' data.txt > event_lines.txt
 - Make in-place change: `Linux` to `LINUX`

`data.txt` content refer from [here](https://en.wikipedia.org/wiki/Linux_distribution)
sed -i 's/Linux/LINUX/g' data.txt
