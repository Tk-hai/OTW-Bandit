# OTW-Bandit
## Level 0
### - In order to ssh into the machine, I used ssh bandit0@bandit.labs.overthewire.org -p 2220 . When running this command you will be prompted to enter a password. Using "bandit0", you will be logged into the machine and met with a welcome screen.
## Level 0 > 1
### - The password for the next level is in a readme file located in home directory.
### - Enter the "ls" command where you will see the readme file. Then, enter "cat readme" to show the password (ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If).
## Level 1 > 2
### - ssh bandit1@bandit.labs.overthewire.org -p 2220 
### - Password : ZjLjTmM6FvvyRnrb2rfNWOZOTa6ip5If
### - The password for the next level is in a file called - located in the home directory
### - "ls" shows a file "-". cat does not return anything so instead "cat ./-" was used to add the path. Password is 263JGJPfgU6LtdEvgfWU1XP5yac29mFx. 
## Level 2 > 3
### - The password is in a file called "spaces in this filename"
### - Using "cat "spaces in this filename"" shows the password MNk8KNH3Usiio41PRUEoDFPqfxLPlSmx.
## Level 3 > 4
### - Password is stored in hidden file in the "inhere" directory.
### - When entering into the "inhere" directory, nothing is shown. 
### - Using "ls -a" does not ingnore entries starting with . 
### - "cat "...Hiding-From-You"" shows the password 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ.
## Level 4 > 5
### - The password is stored in a only human readable file. 
### - Using "ls -la" shows a long list of files. Then use "file ./*" to show the types of all files. One file shows ASCII text, so "cat ./-file07" is used to show the password 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw. 
## Level 5 > 6
### - The password is stored in a file that has the human-readable, 1033 bytes in size, and non executable properties.
### - Checking within the inhere folder shows many folders containing files.
### - Using "file */{.,}* | grep "ASCII text" | grep -v ', with very long lines'" will find files within the folders containing ASCII text. 
### - "du -b -a | grep 1033" will find the file space in bytes. 
### - "cat ./maybehere07./file2" will show HWasnPhtq9AVKe0dmk45nxy20cvUa6EG. 
