### Linux Commands ### 
1. ` uname `
 Tells you about the operating system and the rest of the system.

i) `-a` long version( stands for all)

ii) `-p` Type of processer

2. `whoami`
 It means what type of user you are. 

3. `cat`
It prints out the contents of a file

i) cat /etc/shells - prints the shell type contents

4. `history`
It prints the history of the commands inputted.
i) `history -c : clears the history hence protecting the user's confidentiality

5. `ls`
Lists the file and folders

i) -a lists all hidden files

ii) -l lists in a bulletpoint list with info on all files.

6. `curl`
Transfers data and copies data from the end point.
e.g.: curl https://cdn.britannica.com/39/7139-050-A88818BB/Himalayan-chocolate-point.jpg --output cat.jpg
--output <filename.type>

7. `mv`

Two uses: It can move files and  rename files

8. `cp`
copies a file.
e.g.: cp cat.txt cat.jpg

9. `rm`
removes file / folder.

i) `-f` removes folders.
ii) `-r` removes recursively inside folders.

10. `mkdir`: makes a directory after each argument. 

11)  `touch`
makes a blank file.

12) `nano`
opens up text editor

13) `head`
brings back the specified amount of lines from the top of the file.
i) `head -3` <filename.type> prints the top 3 lines from a file.

14) `tail`
 brings back the specified amount of lines from the bottom of the file.
`tail -3 <filename.type> `prints the bottom 3 lines from a file.

15) `nl`
prints out the number lines of a file.
`nl chicken_joke.txt:`
1 why did the chicken cross the road?
2 To meet the colonel.

16) 
`| "pipe"` allows to add additional commands:

Example: `cat chicken_joke.txt | grep chicken`
It highlights the aspect of the chicken section. 


17) `apt`
  internal linux process to go and get a particular package, and manipulate those packages.

18) `sudo`
super user permissions for a particular command

19) `tree`
shows all directories

20) `-a`  for all

21) `sudo su`
switch user  into super user, typically root user

22) `exit` 
breaks connection to EC2 instance.

23) `Bash`
Born Again Shell - A default shell, with prefix $. This interface allows you to run commands. 
