# 1. Changing File Ownership
`Flag: pwn.college{QrW576lvhiXTdwwzZlwqi46Oaoh.dFTM2QDLzcjN0czW}`
### Method 
I changed /flag ownership using chown to hacker and then used cat.
```
Code: 
chown hacker /flag
cat /flag
```

# 2. Groups and Files
`Flag: pwn.college{ECjMcJDoWpTyyLkaQofyphGfRYR.dFzNyUDLzcjN0czW}`
### Method 
I used chgrp to change hacker to the group that can access /flag then used cat to read it.
```
Code: 
chgrp hacker /flag
cat /flag
```

# 3. Fun with Groups Names
`Flag: pwn.college{AOusP_QCMzs9aA_EyfTS3SMuvp2.dJzNyUDLzcjN0czW}`
### Method 
I used ID to find the grp name and repeated same as previous question.
```
Code: 
id
chgrp grp11887 /flag
cat /flag
```

# 4. Changing permissions
`Flag: pwn.college{Amqby1HM9l3cvdreCqeVP_J4ML9.dNzNyUDLzcjN0czW}`
### Method 
I used chmod to change perission to allow others to read, then used cat.
```
Code: 
chmod o+r *
cat /flag
```

# 5. Executable Files
`Flag: pwn.college{QiPrIzdu3MvZbG-twtjiO7_5k_h.dJTM2QDLzcjN0czW}`
### Method 
This took some thinking because I had assumed that root would be the user and hacker would come under others. Which is why I didn't get the result after changing permission of other to executable. Once I realised the user was hacker, I changed user permission to executable which worked.  
```
Code: 
chmod u+r /challenge/run
/challenge/run
```

# 6. Permission Tweaking Practice 
`Flag: pwn.college{4rt4HpXahjz3ql_sb7SYIxNnCun.dBTM2QDLzcjN0czW}`
### Method 
I ran /challenge/run and followed and edited the chmod command for each requirement 8 times. I got one wrong once so had to redo it, but it was pretty straightforward. Once the 8 rounds were done I used chmod to change read user permissions for /flag and then used cat to read it.

# 7. Permissions Setting Practice
`Flag: pwn.college{wOlG6fxmbN3PaddeVjihBpE4yW3.dNTM5QDLzcjN0czW}`
### Method 
I repeated same as previous question, but using = signs this time, which made it a bit easier. 

# 8. The SUID bit
`Flag: pwn.college{UzMDfKYTMqlUjWpLq7zRhh6yenO.dNTM2QDLzcjN0czW}`
### Method 
I added SUID to u of /challenge/getroot and then ran the command. This opened a new shell where I was the root user. Then I read the flag.
```
chmod u+s /challenge/getroot
/challenge/getroot
cat /flag
```


