# 1. The PATH variable
`Flag: pwn.college{8CU9audixOCDuUYOqK928KzepsO.dZzNwUDLzcjN0czW}`
### Method 
I changed the value of PATH so rm command won't be found, then I ran the command to get the flag.
```
Code: 
PATH=""
/challenge/run
```

# 2. Setting PATH
`Flag: pwn.college{0DNIf3Nk4CfIlGDK-DaVxPpa0pC.dVzNyUDLzcjN0czW}`
### Method 
I set the PATH to the given directory then ran the command to get the flag.
```
Code: 
PATH=/challenge/more_commands/
/challenge/run
```

# 3. Adding Commands
I have spent over an hour trying to solve this but it's simply not giving me the answer. I first tried to create win.sh since it asked me to create a shell script. I used chmod to make it executable but it didn't work. I figured maybe the /challenge/run command only called win and not win.sh. So I tried to create a file win with the read flag command. I tried to set the PATH to win and win.sh, but neither worked. Since they were in the home/current directory, I'm not even sure what to set the path as. 
I used echo "read /flag" > win.sh 
at first, but it didn't give me the output at all.
I tried every possible combination I could think of but couldn't make it work. Since q4 relates to q3, I was not able to solve both these questions. 



