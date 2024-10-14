# 1. Printing Variables 
`Flag: pwn.college{QZHNnmczJSpIb4lJmaFakVpiqrm.ddTN1QDLzcjN0czW}`
### Method 
This was pretty straightforward. I just followed the instructions and put a direct command. 
```
Code: echo $FLAG
```

# 2. Setting Variables 
`Flag: pwn.college{0IIWfbkR_KjS6BzfZtDT2sPgO6T.dlTN1QDLzcjN0czW}`
### Method 
Again I just folowed the instructions, straightforward. 
```
Code: PWN=COLLEGE
```

# 3. Multi-Word Variables 
`Flag: pwn.college{gYkHFrs2Y9YFRggJTtFklyXsSa4.dBjN1QDLzcjN0czW}`
### Method 
I used quotes to assign the text as a single token to the variable.
```
Code: PWN="COLLEGE YEAH"
```

# 4. Exporting Variables 
`Flag: pwn.college{QV9moYo3wM1JiG6sC10BBbzeIY7.dJjN1QDLzcjN0czW}`
### Method 
I exported the PWN variable but not the COLLEGE variable.
```
Code: 
export PWN=COLLEGE
COLLEGE=PWN
/challenge/run
```

# 5. Printing Exported Variables 
`Flag: pwn.college{sDWJ53jKoyp3T9f342H5vty3eMf.dhTN1QDLzcjN0czW}`
### Method 
I used env command and found the flag in the output.
```
Code: env
```

# 6. Storing command output
`Flag: pwn.college{0kZRhca8afup7TX29hmRmN-3LL7.dVzN0UDLzcjN0czW}`
### Method 
I assigned output of command to variable then used echo to print it.
```
Code: 
PWN=$(/challenge/run)
echo $PWN
```

# 7. Reading Input
`Flag: pwn.college{gHCMA3dLtLHL_EuTI1a0Aw5SWMV.dhzN1QDLzcjN0czW}`
### Method 
I used read command.
```
Code: 
read PWN
COLLEGE
```

# 8. Reading Files
`Flag: pwn.college{4wjCn-j-gjaodvF9txeTrdhpLqn.dBjM4QDLzcjN0czW}`
### Method 
I was a little confused at first, but then realised it could all be done in one step, from read to te input value i.e. the command that needed to be run. 
```
Code: read PWN < /challenge/read_me
```

