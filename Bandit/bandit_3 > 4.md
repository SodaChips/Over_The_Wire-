# Bandit 3 > 4
---
## 📌 Overview
The password for the next level is stored in a hidden file in the inhere directory.

<br>

### Objective
  Learn how to change directory and list hidden file
  
<br>

### Command used
  1. `cd [directory]` : change directory
  2. `ls -a` : list all file
     
<br>

### Change directory
  When you use `ls` it will show a directory called inhere. So use `cd inhere` to change directory into it. 
    
  You will noticed that after `cd inhere`, the user side change from  
  ``bandit3@bandit:~$ `` to  `` bandit3@bandit:~/inhere$``  
  Which mean you have change from home directory to inhere

<br>

### List hidden file
  In this directory it show nothing if we use `ls` to list file because the file are hidden.  
  
  Use `ls -a` will list all file including hidden file,  
  ```
  bandit3@bandit:~/inhere$ ls -a
  .  ..  ...Hiding-From-You
  ```

 -  `.` is current directory
 -  `..` is previous directory
 - Password stored in `...Hiding-From-You`.  
Use ``cat ...Hiding-From-You`` will get the password

---
#### Password for bandit4
   xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq
