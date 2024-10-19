# 1. Chaining with Semicolons
`Flag: pwn.college{sLctxg4E4Z43reF4EhrhgfyarIR.dVTN4QDLzcjN0czW}`
### Method 
I directly entered the commands separated by a semicolon.
```
Code: 
/challenge/pwn;/challenge/college
```

# 2. Your first shell script
`Flag: pwn.college{sLctxg4E4Z43reF4EhrhgfyarIR.dVTN4QDLzcjN0czW}`
### Method 
I followed the exact methods mentioned, but it kept recognising it as the previous answer due to it being run in the same order as the last one. To try and avoid that, I used echo with > for first command ten echo with >> to append the second command and then ran it with bash, but it still gave me the flag for the previous question.
```
Code: 
echo "/challenge/pwn" > x.sh
echo "/challenge/college" >> x.sh
bash x.sh
```

# 3. Redirecting Script Output
`Flag: pwn.college{UeDn5EmAhxT4m2IRgVOWkFOHcMj.dhTM5QDLzcjN0czW}`
### Method 
I used ; to connect the two command and enter it into a sh file abc. I then ran it with bash and used | to pipe it to /challenge/solve.
```
Code: 
echo "/challenge/pwn;/challenge/college" > abc.sh
bash abc.sh | /challenge/solve
```

# 4. Executable Shell Scripts
`Flag: pwn.college{oCOCRZxUxGhvER6uwCQNQVw1n6l.dRzNyUDLzcjN0czW}`
### Method 
This took me a lot of time to figure out because I got some minor parts of it wrong. Finally I echo'ed the command to script.sh then used chmod with +x to make it executable then ran it with ./script.sh
```
Code: 
echo "/challenge/solve" > script.sh
chmod +x script.sh
./script.sh
```




