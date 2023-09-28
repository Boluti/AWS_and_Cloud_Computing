### Scripting ###
## Creating a script to install nginx ##
`nano provision. sh ` : It creates the shell script and opens it in nano text editor. 
` #!/bin/bash` : It is placed at the top of the file and tells linux the interpreter to use.
It is called a shbang(tells the operating system,Linux this is going to be a script)
![img_13.png](img_13.png)

## Managing processes in Linux ##
 - Linux is good in managing processes.
 - `$ ps`: It gives information about the process and process ID (PID)
 - `$ ps --help simple`: This will display the help message for the `ps` command, which includes a list of available options, their descriptions, and examples of how to use them.
 - `$ ps -a` : To see all the processes running
 - `$ ps -aux` : it gives a snapshot of the commands. It's best to get a readout 
 - `$ ps -top`: it gives a live readout of the processes.
 - `$ shift and capital M `. It ranks them.  Control z or Control c to stop it from running. Control Q to sign out.
![img_11.png](img_11.png)
 - `$ sleep 5000 &`: This causes the command to run in the background rather than foreground.
 - `$ kill -1 29598(PID number)` : To kill a process from running for example: Sleep.
 - `$ kill -15 29610(PID number)` : Terminates the program entirely( Completely destroyed).
 - `$ kill -9 29610`: It kills the program. It is not recommended on databases.
 - It is recommended to use kill -1 then kill -15. 

 `sudo chmod +x provision.sh - +x` makes file executable.

`./provision.sh` - Run the script once it has been made a executable.

`sudo systemctl status nginx` - We can check the status of nginx

## Permissions ##

- $`ls -l`: Used to see the permissions available.  There are 3 different permissions in linux. The owner(the person who created the file or folder), group permission(sets permissions to group members)
The third set of permission is others. 
Access permission: read(r), write(w) and execute(x) access. 
The owner can read and write but can't execute. The group members can read only. 
- $ `chmod u+x name of the file(bad-joke.txt)`: u+x is for the permissions section(user)
![img_12.png](img_12.png)
- $ `sudo chmod -xw bad-joke.txt`: -xw removes the rights to execute and write
- $ `sudo chmod 777 bad-joke.txt`: 777 gives right to all users to execute. 
- Linux permissions:
chmod-calculator.com to see the shorthand form and code for linux permissions. 
- 776: cannot read and write
- 756: the public can read and write. 
400(Linux permissions): owner can read it.
- 600: Owner can read and write
- 700: Owner can r,w,x
- 770 : Owner and group can both r,w,x
- 760: Group cannot execute but can r,w.
- -767: The public can r,w,x

## Short hand ##
sudo chmod 777 filename - gives all permissions to all sets of users. Each 7 gives all permissions to each user set, so one 7 gives to owners only and and the second 7 gives to group.

Read is 4. Write is 2. Execute is 1. https://chmod-calculator.com/
#  Environment variable #

Environment variable: the name and the contents stored. They are dynamic variables used by a shell and its child processes.
In linux, the variables are all upper case with an equal sign. 
- `$ printenv USER` : prints the user environment variable
- `$ MYNAME=Tife`
- `$ export MY_NAME=Tife` :It declares an environment variable. The name is in the operating system itself and not only gitbash.
- 
