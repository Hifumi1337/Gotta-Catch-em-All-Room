# Title: Gotta Catch'Em All!

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

```

# Questins or Issues
```

```