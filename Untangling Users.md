# 1. Becoming root with su
`Flag: pwn.college{Ip2Jsxa8Faa6DIua-DaL6CmbdnR.dVTN0UDLzcjN0czW}`
### Method 
I used su and then entered the password. I was confued for awhile thinking my system had a problem because it wasn't typing, and then I understood that it doesn't show the password being typed for safety purpouses. I then got root access and used the cat command.
```
Code: 
su
hack-the-planet
cat /flag
```

# 2. Other users with su
`Flag: pwn.college{kTjMgqSc7YSsETYWGLMXyz9_9K5.dZTN0UDLzcjN0czW}`
### Method 
I used su to shift to zardus user and then ran the command.
```
Code: 
su zardus
dont-hack-me
/challenge/run
```

# 3. Cracking Passwords
`Flag: pwn.college{I7ci30fURffKn7MHFQNRHrdnqeb.ddTN0UDLzcjN0czW}`
### Method 
This took a while because it's a new thing that I haven't encountered before. I used john to find the password, then used su to change user to zardus and entered password that john had found. I then ran the command to get the flag. 
```
Code: 
john /challenge/shadow-leak
su zardus 
aardvark 
/challenge/run
```

# 4. Using sudo
`Flag: pwn.college{In8rIcsH1ZLWG_tEHADZYTY8BpS.dhTN0UDLzcjN0czW}`
### Method 
I directly used the sudo command to read the flag.
```
Code: 
sudo cat /flag
```




