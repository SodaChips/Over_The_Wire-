# Bandit 2 > 3
---
## 📌 Overview
  The password for the next level is stored in a file called --spaces in this filename-- located in the home directory
  
### Objective
  Learn how to read content of **file with space among file name**
  
### Problem
  The space between the file name will make terminal misunderstood it was separate items but it was a file name  
  <br>
  So if you use `--spaces in this filename--`, The terminal will read until --spaces and take spaces as a command flag or argument 
  Output (Use ``file`` to find type of file):  
  ```
  file: unrecognized option '--spaces'
  ```
   <br>
   
  Even use `./--spaces in this filename--`, terminal still read it separately and take each word as a file  
  Output (Use ``cat`` to read content of file):  
  ```
  cat: ./--spaces: No such file or directory  
  cat: in: No such file or directory  
  cat: this: No such file or directory  
  cat: filename--: No such file or directory  
  ```
  
### Solution : Contain file path using " "
  We could use "[file path]" to let terminal read whole file path.  
  So ``cat "./--spaces in this filename--"`` will able to get the password
  
---
#### Password for bandit3
  7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME
