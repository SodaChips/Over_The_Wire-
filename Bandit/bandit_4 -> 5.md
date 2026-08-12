# Bandit 4 > 5
---
## 📌 Overview
The password for the next level is stored in the only human-readable file in the inhere directory.  
Tip: if your terminal is messed up, try the “reset” command.

<br>

### Objective
  Learn how to identify file type
  
<br>

### Command used
  1. `cd [file]` : identify file type
     
<br>

### Solution
  After cd to inhere, through ls show there is 10 file
  ```
  -file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
  ```
  
  So, we need to identify which file are human readable instead of cat all of the file  
  ``file ./*`` will list all file type :  
  ```
./-file00: data
./-file01: data
./-file02: OpenPGP Secret Key
./-file03: data
./-file04: data
./-file05: data
./-file06: Non-ISO extended-ASCII text, with NEL line terminators
./-file07: ASCII text
./-file08: data
./-file09: data
  ```  
  Only ACSII text are human readable file, so use `cat ./-file07` to get password

---
#### Password for bandit5
   6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG
