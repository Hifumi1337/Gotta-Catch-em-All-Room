# Title: Gotta Catch'Em All!

# GhostlyPy | Author
```
GhostlyPy is A Web Developer, and Cybersecurity Enthusiast, who enjoys coding with some of his favorite 'weapons;' HTML, CSS, Python, JavaScript, C++ and many more over the years. His preffered ditribution version of linux is Ubuntu and and Kali. This is the first room GhostlyPy has ever done!

YouTube: https://www.youtube.com/channel/UCnMcOdlU57Bsa5-rbyY7Neg
Twitter: https://twitter.com/GhostlyPy
```

# Description
```
This room is based off the original Pokemon series. Can you obtain all the Pokemon in this room?
```

# WriteUp *Past this point ALL tasks will be revealed*

# Task 1
```
Run nmap to search open ports

nmap -sC -sV -Pn (The server DOES ping, I just prefer -Pn)

After running an Nmap scan we'll see that there is an ssh & http port open. We will utilize both of these ports for this room.

Open the IP in your browser of choice, click 'open page source' or the equavalent in your browser

Scrolling all the way to the bottem shows a weirds combination of username and password. Could this be a user?

After logging into the ssh with the provided credentials, change the directory to /home/

Why is there a zip file here? Lets unzip it!

This will have our first pokemon's text file!

Wait. It still requires a hesadecimal decoder to find the answer. After doing so, you'll have your pokemon!
```

# Task 2
```
Easy.

Run the following command:

gobuster dir -u {Machine-IP} -w <Location of preffered Wordlist>

You'll find theres a webpage on the server called http://{Machine-IP}/<Text-File-Name>

Wanna find it easier? Maybe the file name is similar to the question like the first task seemed to be.

This one is encoded to, but looks a lot weirder. That's because it's a caesar cypher!

After decoding using the 14th shift, you'll have your pokemon!
```

# Task 3
```
Still logged into the same user

Move over to the / directory, and there will be a really weird directory located there.

After changing into the weird directory, you'll see the file!

This one needs to be decoded using base64.
```

# Task 4 - LAST ONE!
```
Let's go back to that home directory and see if we can find any log creds for a second root user

Defiitely a weird directory in /Videos.

Absolute path: Gotta/Catch/Them/ALL!

Hmm, this looks like a fake C++ file! Maybe it has something in it!

cat Could_this_be_what_Im_looking_for?.cplusplus

There's the login credentials!

Time to become Ash Ketchum and gain root (again) access and the final flag

Now we need to change the directory to 'home' (Can't use ~)

There it is! The final flag!

Best thing about this flag? No cypher or coded message!

Congratulations!
```

# Questins or Issues
```
Please let me know if any bugs or problems occur during your CTF.
You can message me on the TryHackMe website or use the issues tab located in the Options tab.
Thank you.
```