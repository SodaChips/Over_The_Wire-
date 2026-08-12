# Bandit 1 > 2
---
## 📌 Overview
The password for the next level is stored in a file called - located in the home directory
  
### Objective
  Learn about command flag and how to specify a file
  
### Command flag
  To understand command flag, here is the different for output of `ls` and `ls -a`  
    
  Output of ls:  
  ```
  -
  ```

  Output of ls:  
  ```
  -  .  ..  .bash_logout  .bashrc  .profile
  ```

  You will noticed that `ls -a` will list out more file than `ls`. As it use command flag `-a` which stand for **list all**  
  To know more command flag for `ls`, you may use `ls --help`  
    
  *The main thing you should learned is every command flag are using -*
  
  
### Apply to situation
  The file called **-**  
  if you use `cat -`, the terminal will take it as command flag.
  
### Solution
  Use command `cat ./-`  
  It will specify that **-** is a file by using its path (./ means current directory)

---
#### Password for bandit2
    PK8fYLZg2hnHSz83plBL1iEPKdD3QToB
