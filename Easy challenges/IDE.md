# IDE

Time: 45 minutes

Difficulty: Easy

## What is about?

This challenge test or skill of penetrating. The challenge does not give much explanation about the current state that we are and just give us the goal which is gain a shell and escalate our privileges.

## Challenge

To gain control on the shell we first need to know what ports are open. We scan all the ports with nmap and we encounter the the port 21 is using the service ftp. Exploring on the internet I learn that this service allow the user the send of files. But one thing that is interesting is that he is not using the secure service so we can see the files.

To do that we need to have installed ftp and do `ftp -a MACHINE_IP` to enter the service as Anonymus. We encounter some folders and if we search in the folders we find a file with the name `-`, so we get that file to our computer and we open it. Inside the file it was a letter from Drac to Jonh telling him that he just reset his password and now it is the default password.

![Letter](../images/Captura%20de%20pantalla%202026-08-25%20225513.png) 

This information is important because now we know is name and that the password is on default, now we go to a page that I did not tell before when I did the nmap. This web is on the port 62337 and we can see that is a login page.

![Web](../images/Captura%20de%20pantalla%202026-08-25%20231551.png) 

So we know is name but not the password but is no default, for this problem Hydra will help us. I pass Hydra the IP and a rockyou.txt for the password with this command ` `, and it gave me that the password is `password`. We enter with this credentials and we are in. 

-----------Still in progress---------

## Conclusion
