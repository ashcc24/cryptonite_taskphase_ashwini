# cat command 
used cat /flag to give the flag 
# carting absolute paths 
used cat /flag 
# more catting practice 
they gave the file location, so i copied tat along with the cat command at the start. i basically used it as an absoulte pathname diretly instead of jumping to that directory first and then running cat command 
# needle in a haystack 
i used grep with the substring pwn.college as thats how every flag starts, then typed the file location as given in the instructions to get the flag
# listing files 
i struggled quite a bit ith this one. i used ls /challenge first and got two files. I had to cd to challenge directory. i used cat on both and found the command used to display the flag, but not the flag itself. i tried to access the files but couldnn't. After a lot of back and forth i realised I needed to run the file using absolute pathnae. so while I was in the /challenge directory, i used ./ and ran the renamed file, which eventually gave me the flag. 
# touching files 
i created tmp using touch, then used cd to change directory to tmp. then i separately created the files pwn and college. then ran /challenge/run to get the flag 
# removing files 
I used ls to check the files, then rm to remove the required file and ten ran challenge/check to get the flag 
# hidden files 
I struggled a bit with this one as well, because  kept using ls -a directly. it took me a while to realise that i had to use cd / and then use ls -a. then thee was a file that had flag with some numbers, i used cat to read the flag.
# epic filesystem quest 
this took me an insanely long amount of time, but it got much easier as i went along. I mostly used cd to shift to the directory given in the clue and then used ls to find the clue file, then used cat to read it. In the 'trapped' clues that wod self destruct with the use of cd, I decided to use ls or ls -a followed by the path to be able to see the files. I then repeated the same code but with cat instead of ls so I could directly read the clue file without transferring to that directory. I continued this over and over till I finaly reached the final clue and captured the flag. 
# making directories 
i used mkdir /tmp/pwn then touch /tm/pwn/college then used /challenge/run to find the flag 
# finding files 
flag-pwn.college{ARas5IV6_9LCmNIajvD4Nr0PjLw.dJzM4QDLzcjN0czW}
i used find / -name flag and it gave me a huge list. Most of them said permission denied. I went through the ones where permission wasn't denied and I used cat individualy on each one till i found the flag.
# linking files
flag- pwn.college{U6WGlmI9zIACgaq8woxW4Hnb0Lb.dlTM1UDLzcjN0czW}
i used ln-s /flag /home/hacker/not-the-flag to trick the link into giving me the right flag. i then ran the /challenge/catflag
