## Bandit 17 > 18
At this level (Level_17 -> Level_18) we know that there are two files in home directory, which is passwords.old and passwords.new.  
The passwords for next level are in the passwords.new that only one line different between passwords.new and passwords.old.  

# Information
- Two text file :   
  passwords.new  
  passwords.old
- Find the different between them
- The passwords.new in the result is password for next level

# Solution
So we could use 
```bash
diff passwords.new passwords.old
```
to grep the different between these two files.

# Result
The result come out with :
```bash
< x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO
	---
> pGozC8kOHLkBMOaL0ICPvLV1IjQ5F1VA
```
# Log in bandit18
The line start with `<` is the line in passwords.new which is our password for next level.  
When you try to use this password to log in bandit18, it will unsuccesful and you will see 'Byebye!'.  
Don't worry about it, it doesn't mean the password is wrong. Instead, you are solved this level.  
But...why it couldn't log in bandit18? It will be solved and explain in next level (bandit_18 ->19)
