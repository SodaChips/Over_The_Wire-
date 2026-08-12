# Bandit Level 0

Due to OTW change the password, I need to do whole bandit again🥲🥲. So I do this writeup while Im at it

---

## Overview
The goal of this level is for you to log into the game using SSH. The host to which you need to connect is  
bandit.labs.overthewire.org, on port 2220. The username is bandit0 and the password is bandit0. Once logged in,  
go to the Level 1 page to find out how to beat Level 1.
### Objective
Learn how to use SSH to login a host

### Command used
```ssh [userName]@[host] -p [portNumber] ```  
then enter the password

### Apply to question
- user : bandit0  
- host: bandit.labs.overthewire.org  
- port: 2220  
- password: bandit0  
  
```ssh bandit0@bandit.labs.overthewire.org -p 2220```


