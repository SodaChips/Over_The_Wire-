# Bandit 6 > 7
---
## 📌 Overview
The password for the next level is stored somewhere on the server and has all of the following properties:
```
owned by user bandit7
owned by group bandit6
33 bytes in size
```
<br>

### Objective
  Learn to apply options of find to filter the file based on the owned user and group
  
<br>

### Command used
  1.  find --help : to find out what option can used
  2. `find [starting_point] [options]` : apply options or filter to find the file based on its properties
     
<br>

### Observe environment
 There will be nothing if I'm using `ls`. So, we can't find out the password from current directory.  
 Thus, we need to find from root directory (/)
 
### Solution
We gonna use
```
find / -user bandit7 -group bandit6 -size 33c
```  
  1. ``/`` : start find from root directory  
  2. ``-user bandit7`` : the file is **owned by user bandit7**  
  3. ``-group bandit6`` : the file is **owned by user bandit6**
  4. ``-size 33c`` : the file size is **33 bytes**

After that, there will be a lot of `Permission denied`. But, there is an accessible file
```
/var/lib/dpkg/info/bandit7.password
```

So we could just ``cat /var/lib/dpkg/info/bandit7.password`` to get the password
     
---
#### Password for bandit6
   Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3
