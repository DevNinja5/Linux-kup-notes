# Awk, Sed and Grep commands
1. [awk](sed-grep-awk.md#awk)
2. sed
3. grep

## awk
**Let's create a file first**
```
cat > test.txt
```
Add data in this `test.txt`
```text
ajay manager account 45000
sunil clerk account 25000
varun manager sales 50000
amit manager account 47000
tarun peon sales 15000
deepak clerk sales 23000
sunil peon sales 13000
satvik director purchase 80000 
```

* To print lines having `account` word 
```
awk '/account/{print $0}' test.txt
```
output will look like
```text
ajay manager account 45000
sunil clerk account 25000
amit manager account 47000
```
---
* To print 2nd field of file 
```
awk '{print $2}' test.txt
```
Output Will look like:
```text
manager
clerk
manager
manager
peon
clerk
peon
director

```
---

* To print first field of each record whose second field contains “manager”
```
awk '$2 ~ /manager/ { print $1 }' test.txt
```
Output will look like :
```
ajay
varun
amit
```
---

* To print number of lines in file
```
awk 'END { print "File", FILENAME, "contains", NR, "lines." }' test.txt
```
Output will look like:
```
File test.txt contains 8 lines.

```
---
To Print rows from 2 to 5 
```
awk 'NR==2, NR==5 {print $0}' test.txt
```
Output will look like:
```
sunil clerk account 25000
varun manager sales 50000
amit manager account 47000
tarun peon sales 15000
```
---
