# Bandit 5 > 6
---
## 📌 Overview
The password for the next level is stored in a file somewhere under the inhere directory and has all of the following properties:  
```
human-readable  
1033 bytes in size  
not executable  
```
<br>

### Objective
  Learn to apply options of find to filter the file
  
<br>

### Command used
  1. `find [starting_point] [options]` : apply options or filter to find the file based on its properties
     
<br>

### Observe environment
  After cd to inhere, through ls show there is 18 directory
  ```
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
  ```
  
  It different from 10 file because there could be multiple file in each directory,  
  lets use ``ls *`` find out how many file there is
  ```
  maybehere00:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere01:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere02:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere03:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere04:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere05:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere06:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere07:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere08:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere09:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere10:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere11:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere12:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere13:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere14:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere15:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere16:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere17:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere18:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

maybehere19:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
  ```

  Obviously, is impossible that we cat each file in each directory one by one

### Solution
Hence, we need to use ``find`` to find out the file match with properties provided.  
  
```
find . ! -executable -size 1033c -exec file {} \;
```  
  1. ``.`` : start find from current directory  
  2. ``! -executable`` : the target is **not executable**  
  3. ``-size 1033c`` : the size of target is **1033 bytes**  
  4. ``-exec file {} \;`` : execute command `file` for each found to show its file type  
  
 Result : ``./maybehere07/.file2: ASCII text, with very long lines (1000)``

And ``cat ./maybehere07/.file2`` will get the password
     
---
#### Password for bandit6
   pXa26xhMWaC2SvDotA4r9EgZkulOeSBW
