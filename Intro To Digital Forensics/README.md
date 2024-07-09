
# Capstone Project
## [Scenario](https://github.com/alejandro-garf/Blue-Team-Junior-Analyst/blob/main/Intro%20to%20DarkWeb%20Operations/Scenario)
## [Certificate](https://github.com/alejandro-garf/Blue-Team-Junior-Analyst/blob/main/Intro%20to%20DarkWeb%20Operations/IntroToDarkwebOPs.pdf)
### Setting Up
 - Booted up my Vm
 - Downloaded the drive zip file.
### First piece of evidence 
 - we had a hint to check the saved emails first
 - A legit looking email but with an attachment name Form1.jpg, used file command amnd confirnmed it’s jpg only
 - Used strings command to extract the strings from the Form1.jpg. Found our first piece of evidence
```
“Simon, I have usernames and passwords for the VPN. Still on my work PC. Don’t want to risk emailing them just yet. When I do, the file is a .jpg image + password for extraction is password
. Use steghide. Talk again soon”
```
### Second Piece of Evidence 
 - Used the hint and went to images folder
 - After trying to crack stego, lapotop.jpg was the only one got crackes with passphrase “password”
 - As he said there are vpn passwords of users
### Third Piece of Evidence 
 - After a while of searching through folder found a suspicous looking xml file
 - Used the file command and found it was origibally a png image
 - Converted it to a png image using mv command
 - Opened image and found locations of UK Offices
### Fourth Piece of Evidence
 - Found a hidden file named ‘ .a0415ns.zip’ at /WebDev work/unfinidhed webpages/to-do/
 - Tried to unzip, but password protected
 - Cracked the Password using dictionary attack
 - Unziped the file and got employeedump which contained employee information.
### Fifth piece of evidence
 - After searching into each folders and opening each files, finally i found this file named bootstrap.min.abc
 - It's a ss file at WebDev work/unfinished webpages/templatemo_508_power/css
 - cat it
```
└─$ cat bootstrap.min.css
/*!
 * Bootstrap v3.1.1 (http://getbootstrap.com)
 * Copyright 2011-2014 Twitter, Inc.
 * Licensed under MIT (https://github.com/twbs/bootstrap/blob/master/LICENSE)
 */

/*!
 * This is in case Colin tries to screw me. I'll expose him.
 * Colin Andrews
 * 31 years old
 * lives in Suffolk, UK
 * drives a Kia Sportage
 * buys and sells valid company credentials to hackers
 * phishing attacks, malware distribution

 * (still got his email addresses, domains, mobile no. and BTC wallet address on my personal PC)
 */
```

### This concluded all of the evidence gathering for this digital forensics capstone project
