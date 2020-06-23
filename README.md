# Title: Gotta Catch'Em All!

# GhostlyPy | Author

GhostlyPy is a Web Developer and Cybersecurity Enthusiast who enjoys coding with some of his favorite languages, including HTML, CSS, Python, JavaScript, C++, and many more over the years. His preferred distribution version of Linux is Ubuntu and Kali. This is the first room GhostlyPy has ever done!

YouTube: https://www.youtube.com/channel/UCnMcOdlU57Bsa5-rbyY7Neg (Videos have been recorded, will be up very soon!)
Twitter: https://twitter.com/GhostlyPy


# Description

This room is based on the original Pokemon series. Can you obtain all the Pokemon in this room?


# WriteUp (Past this point ALL tasks will be revealed BUT no answers)


# Task 1

Run Nmap to search open ports

**nmap -sC -sV -Pn {Machine-IP}** (The server DOES ping, I just prefer -Pn for silence)

After running a Nmap scan, we'll see that there is an ssh & HTTP port open. We will utilize both of these ports for this room.

Open the IP in your browser of choice, click 'open page source' or the equivalent in your browser.

Scrolling to the bottom shows a weird combination of username and password. Could this be a user?

After logging into the ssh with the provided credentials, change the directory to /home/

Why is there a zip file here? Let's unzip it! (Sometimes the file is already unzipped if so, it should still work).

**unzip <file_name.zip>**

This will have our first pokemon's text file!

Wait.

It still requires a hexadecimal decoder to find the answer. After doing so, you'll have your pokemon!

Hexadecimal Decoder: https://cryptii.com/pipes/hex-decoder


# Task 2

Easy.

Run the following command:

**gobuster dir -u {Machine-IP} -w <Location of preferred Wordlist>**

You'll find there's a webpage on the server called http://{Machine-IP}/<Text-File-Name>

Wanna find it easier? Maybe the file name is similar to the question like the first task seemed to be.

This one is encoded too, but looks a lot weirder. That's because it's a Caesar Cipher!

After decoding using the 14th shift, you'll have your pokemon!

Caesar Cipher Decoder: https://cryptii.com/pipes/caesar-cipher


# Task 3

Still logged into the same user:

Move over to the '/' directory, and there will be a weird directory located there.

After changing into the weird directory, you'll see the file! (You'll know the weird directory, trust me).

This one needs to be decoded using base64.

Base64: https://www.base64decode.org/


# Task 4 - LAST ONE!

Let's go back to that home directory and see if we can find any login credentials for a second root user.

Definitely a weird directory in '/Videos/'.

**Absolute path: 'Gotta/Catch/Them/ALL!'**

Hmm, this looks like a fake C++ file, maybe it has something in it!

**cat Could_this_be_what_Im_looking_for?.cplusplus**

There are the login credentials!

Time to become Ash Ketchum and gain root access (again) and the final flag.

Now we need to change the directory to 'home' (Can't use ~).

There it is! The final flag!

The best thing about this flag? No cipher or coded message!

# Congratulations!


# Thank You So Much For Playing My First Room!


# Questions or Issues
```
Please let me know if any bugs or problems occur during your CTF.
You can message me on the TryHackMe website or use the issues tab located in the Options tab.
Thank you.
```