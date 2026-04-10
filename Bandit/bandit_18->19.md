## Bandit 18 > 19
At last level we faced a problem which is the terminal will pop up 'Byebye!' and log us out when we try to log into bandit 18  
From OTW website we know that the password for the next level is stored in a file **readme** in the homedirectory of bandit 18

# Information
- password in file **readme**

# Understanding main problem
Since,  `.bashrc` of bandit 18 has been modified to log us out when we log in with SSH. So, we should think another way that we can get information from bandit 18 without logging into it  
(Actually I always want to try login through another way when I first time play this level, but the solution is easier than I think)

Here is something we need to understand before we start to solve it   
The process that we log in through SSH will start with SSH authentication. Once it success, the server will start bash and we could use the CLI of bandit 18  
But due to the `.bashrc` has been modified (`exit` when we login) , so we couldn't login with SSH

# Solution  
The solution for this problem is......we just append our command to the SSH connection code (Too easy right? :) )  
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 (command)
```  

For an example, I want to confirm that the **readme** file is in the homedirectory of bandit 18. I could use  
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 ls
```  
The result : 
```bash
readme
```  
<br>
<br>

So, I can just get the pssword with command   
```bash
ssh bandit18@bandit.labs.overthewire.org -p 2220 cat readme
```  
The result : `cGWpMaKXVwDUNgPAVJbWYuGHVn9zl3j8` 

# Explaination
SSH has two modes which is **Interactive Shell Mode** and **Non-interactive Command Execution Mode**
- **Interactive Shell Mode**  
    When we login with `ssh user@host`,  
    the server will start a shell such as bash and execute `.bashrc`
  
- **Non-interactive Command Execution Mode**   
    When we login with `ssh user@host (command)`,  
    we bypass the shell and execute the command directly
    





