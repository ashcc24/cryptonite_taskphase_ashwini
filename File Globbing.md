# matching with *
flag- pwn.college{gVdHBEJU7qUm6PWP0aHq654QBeP.dFjM4QDLzcjN0czW}
i used cd/ch* to change directory then ran /challenge/run command 

# matching with ?
flag- pwn.college{8YCTwDLo4aKafX-ydsz7uxZ5jAk.dJjM4QDLzcjN0czW}
i used cd /?ha??enge and then ran /challenge/run to find the flag

# matching with []
flag- pwn.college{w1xwDHe4v6X2-ANcG8LyfkeDsYe.dNjM4QDLzcjN0czW}
i struggled a bit with the format but understood the logic pretty quickly. I used cd to change directory then used /challenge/run file_[b,a,s,h] to get the flag.

# matching paths with []
flag- pwn.college{oBov0Nxs42ol9CSl8-m1MtUkJL3.dRjM4QDLzcjN0czW}
after trying different combinations of the command, what finally worked was
/challenge/run /challenge/files/file_[bash]

# mixing globs
flag- pwn.college{oaagqrqOBZKKhhVXZMV5gA2-uIt.dVjM4QDLzcjN0czW}
this took me a lot of time. It kept saying too may caracters or giving me errors. Finally what worked was putting the first letter of the three words within [] and a * outside. 
i.e.  /challenge/run [cep]*

# exclusionary globbing 
flag- pwn.college{kitsRURb8J7clrmkDj4vCEfC8M1.dZjM4QDLzcjN0czW}
i used the same logic as previous one but with a ! to get the flag