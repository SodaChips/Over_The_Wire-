## Bandit 18 > 19
At last level we faced a problem which is the terminal will pop up 'Byebye!' and log us out when we try to log into bandit 18  
From OTW website we know that the password for the next level is stored in a file **readme** in the homedirectory of bandit 18

# Information
- password in file **readme**

# Solution
Since,  `.bashrc` of bandit 18 has been modified to log us out when us log in with SSH. So, we should think another way that we can get information from bandit 18 without log into it  
(Actually I always want to try login through another way when I first time play this level, but the solution is easier than I think)

Here is some new thing we will learn  
the process that we log in through SSH will start with SSH authorization. Once it success, the server will read the bash and we will get the CLI
