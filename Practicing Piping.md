# redirecting output
flag-pwn.college{I0uJETRL9Aec9SMMlYp0Sg0p2r-.dRjN1QDLzcjN0czW}
pretty straightforward, i used echo PWN > COLLEGE

# redirecting more output
flag- pwn.college{Exvm5U6IB7JHlQ1mbJWFiDxsqSz.dVjN1QDLzcjN0czW}
i used /challenge/run > myflag to write output in myflag. then i used cat myflag to extract this output

# appending output
flag- pwn.college{UDlFbGME8Qp9tibEsHKxqUGHN46.ddDM5QDLzcjN0czW}
i did same as above which wrote the first haf of flag. i then repeated the command with >> instead of > which appeded second half. I then used cat to get the flag.

# redirecting errors 
flag- pwn.college{QYoXNqMalyB6VrYL7Md6fbSzMxb.ddjN1QDLzcjN0czW}
i did both the redirecting in 1 step as /challenge/run > myflag 2> instructions

# redirecting input 
flag- pwn.college{cFLwg8AUFJvWgWYabO3vYTZoZVv.dBzN1QDLzcjN0czW}
I used echo COLLEGE > PWN to write the data first and then /challenge/run < PWN which gave me the flag

# grepping stored results 
flag- pwn.college{UZtc89h8R--ijAWrWu0v32mRODS.dhTM4QDLzcjN0czW}
I did std output using > then used grep with the substring pwn.college in the file tmp,data.txt to find the flag

# grepping live output
flag- pwn.college{ImiqYRprHtFYnr7PMoJKdXIyHaW.dlTM4QDLzcjN0czW}
i used pipe operator and grep directly with substring as pwn.college. it gave me the flag directly. command used was /challenge/run | grep pwn.college

# grepping errors
flag- pwn.college{YSbevu9RFAkTyeKjg-K2gsGFwtT.dVDM5QDLzcjN0czW}
I folowed the instrutions iven and it was a straightforward code 
/challenge/run 2>&1| grep pwn.college

# duplicating piped data with tee
flag- pwn.college{M53cFSiLSBjKt5NST8B2bgdQGhO.dFjM5QDLzcjN0czW}
i found this quite tricky for some reason. I used | to write input to output but it wasn't working. I used tee command as such
/challenge/pwn | tee challengeop | /challenge/college
and then did cat challengeop to get the secret code. I then used that to write onto output and got the flag

# writing to multiple programs
flag- pwn.college{A2WQKfEaw5IPF6fk5cL9WKRngDl.dBDO0UDLzcjN0czW}
I did some trial and error, and the command that worked was
/challenge/hack | tee >( /challenge/the ) | /challenge/planet
i used tee to duplicate the data, > to write it onto the command, and | to write it to planet. 

# split piping stderr and stdout
flag-pwn.college{cZfMjqOhcgqmGtewN-YrHk59TVO.dFDNwYDLzcjN0czW}
/challenge/hack > >( /challenge/planet ) 2> >( /challenge/the )
this took me a long time to piece together. i did it in parts till it was successful. 
first part would obviously be /challenge/hack 
i then used > to rediret the std output. from there it does 2 different things,
first i did >(/challenge/the) so it would write the output there. then 2> is used to redirect the stderr, and similar to previous step >( /challenge/the ) is used to write the error output there. 
