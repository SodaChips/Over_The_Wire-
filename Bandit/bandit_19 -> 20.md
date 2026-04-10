## Bandit 19 -> 20
To gain access to the next level, you should use the setuid binary in the homedirectory. Execute it without arguments to find out how to use it. The password for this level can be found in the usual place (/etc/bandit_pass), after you have used the setuid binary

# Information
- A setuid binary in homedirectory of bandit 19 (without argument to know how to use)
- password stored in ``/etc/bandit_pass/bandit20``

# Solution
1. As usually, we start with 
  ```bash 
  ls
  ```
  know what file are in homedirectory  
  ```bash 
  bandit20-do
  ```
<br>
<br>

2. So we know that `bandit20-do` is the setuid binary we gonna use  
Lets execute it without argument
  ```bash
  ./bandit20-do
# ./ means current directory
  ```
 and we will get the result 
 ``` bash
Run a command as another user.
  Example: ./bandit20-do whoami
```
<br>
<br>

3. We could try the example
   ```bash
   ./bandit20-do whoami
   ```
   the result will be
   ```bash
   bandit20
   ```
   which mean we have privilege as bandit20 when we use the setuid binary<br>
<br>
<br>

4. Since, we can use the privilege of bandit20 to `cat` its password from `/etc/bandit_pass`
   <br>
   
   ```bash
    ./bandit20-do cat /etc/bandit_pass/bandit20
   ```
     The result:`0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO`
