# 1. Listing Processes
`Flag: pwn.college{4cWyV_zSjGOEQKv26NmEHYFoNeg.dhzM4QDLzcjN0czW}`
### Method 
I followed the given instructions exactly, used ps aux, found the filename which seemed likely to contain the flag, and then ran it.
```
Code: 
ps aux
/challenge/11780-run-18595
```

# 2. Killing Processes
`Flag: pwn.college{YRD_Zdg7zdjvw-id9D-f2ZHm02w.dJDN4QDLzcjN0czW}`
### Method 
I was confused about what to do, because I tried to use the same syntax as given in the example i.e. `ps -e | grep /challenge/dont_run` but it didn't give me an output. So I used ps aux to list all the processes ad found the PID of /challenge/dont_run from there and used it to kill the process. 
```
Code: 
ps aux
kill 73
/challenge/run
```

# 3. Interrupting Processes
`Flag: pwn.college{o68U9oRTo-cfWwEPLb6U7HMPczp.dNDN4QDLzcjN0czW}`
### Method 
I ran the command then hit Ctrl C.
```
Code: 
/challenge/run
^C
```

# 4. Suspending Processes 
`Flag: pwn.college{MnSepPmowtsl-hxRJfTnawf1ikG.dVDN4QDLzcjN0czW}`
### Method 
I started the command then did Ctrl Z, then ran command again.
```
Code: 
/challenge/run
^Z
/challenge/run
```

# 5. Resuming Processes
`Flag: pwn.college{w4hAGAPptlWOoHeEiIhkyPCn5l4.dZDN4QDLzcjN0czW}`
### Method 
First run the command, then use Ctrl Z and then fg. 
```
Code: 
/challenge/run
^Z
fg
```

# 6. Backgrounding Processes
`Flag: pwn.college{4nlDeyBKOA4vvssfMFgKdrIDPKw.ddDN4QDLzcjN0czW}`
### Method 
I ran the command, used Ctrl Z, then used bg to make it run in the background. I then ran the command again. 
```
Code: 
/challenge/run
Ctrl Z
bg
/challenge/run
```

# 7. Foregrounding Processes
`Flag: pwn.college{gdclN0WxwT5dVbQv4yd6yz0BWDF.dhDN4QDLzcjN0czW}`
### Method 
I ran the command, did Ctrl Z to suspend it, then used bg to run it in the foreground, then used fg to push it to the foreground.
```
Code: 
/challenge/run
Ctrl Z
bg
fg
```

# 8. Starting background processes
`Flag: pwn.college{41ZrfBJnegPXPTZs1s2oDHlXTwK.dlDN4QDLzcjN0czW}`
### Method 
Direct command. 
```
Code: /challenge/run &
```

# 9. Process exit codes
`Flag: pwn.college{88ghUVD-0O-ZwqVO8JoKfYbP2I9.dljN4UDLzcjN0czW}`
### Method 
I ran the get code command first, then used $? to get exit code which I then used as an argument for the submit code command. 
```
Code: 
/challenge/get-code
echo $?
/challenge/submit-code 110
````

