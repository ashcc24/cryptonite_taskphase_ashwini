I have gone through the solution writeups, the discord server, and searhed things that I didn't understand initially or why they were being done that way (which was most of it). Eventually I understood the logic behind the solutions and tried to explain each one below. I was told to start somewhere in between and do 10 chaenges, so I have done 15 to 24. 

# 15 Not Noice 
From what I understood, the challenge will originally be in a .wav file. Using a audio editing software like audacity will help us open the file, after which we can select spectogram, which shows the changing frequencies format instead of the reular amplitudes pattern. This will reveal any hidden code. 

# 16 Nom Nom
It seems to be a case of inspect, which as far as I know changes the details on the screen of the client end. Cookies are used to store data, and here an existing value of a cookie needs to be changed to True (probably a boolean value) and refreshed. I am not exactly sure how one would realise that this needs to be done. 

# 17 Quench your thirst 
Here I copy pasted the text onto a cipher identifier and it gave a certain type of cipher. I entered the text into its auto solver and it gave me the proper text. However the link was jumbled. 4 of the letters were not repeated elsewhere, so all combinations would need to be tried to be able to get the proper link. 

# 18 Git Gud
The git log contains commit messages that are updated every time a change is made to the repository. The flag is hidden in there. Using a combination of grep, tac (to reverse order of lines), and -d to remove unnecessary things and give the flag we get the answer. The final flag seems to have a fun message too, written with numbers that look like letters. It says something like get gutter/better at git.

# 19 Stairway to Heaven
This contains an executable game that I am not able to open, but its given that it spits out random colours. Initially I didn't understand what they meant in the solution section. I eventually realised they meant that the text is in the same colour and format as the background in such a way that its hidden; we can't see it.
Since I cannot access the game I'm not too sure of te method we need to use to uncover the text, but if possible maybe we could redirect it into a text file output then read it. There also seems to be a command cat -v used to print usually unprinted text. Since the flag would be in ASCII code, I'd then either have to manually decode it or run a program to get the flag. 

#20 Firewall Jail
The solution seems to be to change the userid to -1. This can be done probably using developer tools in the browser or some external site. After some research, I think the logic behind changing it to -1 is that sometimes certain values are **unexpected** or **out of range** such as negative numbers which might just give us access to sensitive data, or allow us to exploit a weak unsecure part of the code. 

# 21 Heads up, Tails down
The solution states that it is actually a png file that has been corrupted. Through some research it seems that every png file needs to have a certain 8 leading characters without which the header would be wron and file would be corrupted. Hence, opening it ina hex editor which allows us to edit at a binary level will help me manually fix the header and view the file. 

# 22 All that for a drop of blud
This seemed more complicated and I really had to dig deep to be able to understand what the steps meant exactly. 
First we needed to change UserAgent to OASISPlayer. This needs to be changed in the URL header. It helps identify the client making the request. We can use browser developer tools.
Then we need to send a POST request. It will reply with various parameters that need to be used, and we must append them onto our POST request. 
It seems like the simpler way to do all this is to use an external site for testing this out and changing the URL's and other parameters.

# 23 A Rokcy Start
This is a rigged version of the game where I can only proceed if I somehow manage to reach the score of 100. I had to earch and understand the concept of buffer overflow to understand the concept.
If I manage to input enough data such that the name field overlows, I wil be able to change the score data. Using pretty much a trial and error method of how various inputs affect the score, I could get an idea of where the score memory is located.
Here its 25 bytes ahead of the name memory, which means I would need to enter an input large enough (for 25 bytes) to bypass it.

# 24 Comma separated virus
It is a long list of comma separated valuesa among which the virus is hidden. Emphasis is given on using various EDA techniques to sort through. It is suggested to use pandas, which is a pytho library that will help sort through the values. It has various functions that will be useful in finding the flag. 




