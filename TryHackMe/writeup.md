#connect to 10.10.183.175

#Step 1: Connect to server

#Step 2: Find vulnerabilities

#Step 3: Run nmap to find open ports on target server
'''
22
80
139
445
8009
8080
'''
Using dirbuster, found "development" directory

#Step 4: Brute force for usernames
'''
No Answer Needed
Use enum4linux to find out all information about the given machine
/use/share/enum4linux/ -a *address* | *save to log file
Finds 2 users: Jan, Kay
'''

#Step 5
'''
From the message on the website we know the Jan "J" has a weak password
'''

#Step 6: What is the password?
'''
We can use hydra in order to brute force the users password. I chose to use the rockyou wordlist
User: jan
Password: armando
'''

#Step 7: SSH is used to remote access servers 

#Step 8: No answer needed

#Step 9: Other use we found way Kay

#Step 10: No answer needed

#Step 11: What is the final password (Kay's password)
'''
After logging in to jay using ssh we are able to find the ssh file for kay. 
Copying the ssh file and trying to open it we find that it's password protected.
Using john the ripper and the rockyou wordlist we are able to crack the password for the ssh key which allows us to log in as kay
Looking at their home directory we can open the pass.bak file which will reveal the final password
'''