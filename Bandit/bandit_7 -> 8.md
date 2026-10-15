# Bandit 7 > 8
---
## 📌 Overview
The password for the next level is stored in the file data.txt next to the word **millionth**  
<br>
  
### Objective
  Learn to use grep to grab certain line of word with selected text
  
<br>

### Command used
  1. `grep [selected text] [options]`
     
<br>

### Observe environment
1. After using `ls` and `wc-l` we know that there is only one file, data.txt with 98567 lines.  
2. For our information, the password is following a word "millionth" in the data.txt.  
**( Beware not millionth of word in the file 😂😂 because its my mistake )**  
  
### Solution
We gonna use
```
grep millionth data.txt
```  
which will grab the line of words included "millionth" in data.txt

The result
```
millionth       VR1ljMayciFxbnUokuQmJFw6QC9VKtub
```

Obviously, there is the password
     
---
#### Password for bandit8
   VR1ljMayciFxbnUokuQmJFw6QC9VKtub
