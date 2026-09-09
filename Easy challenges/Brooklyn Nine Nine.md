# Brooklyn Nine Nince

Time: 25 minutes

Difficulty: Easy

## What is about?

This challenges just gave the instruction of hacking into the machine and escalte priviligies. Supposedly there are many ways in doing this room.

## Challenge

First I started with a nmap like always and i noticed we have the service ftp so we enter as anonymous with the command `ftp -a MACHINE_IP`. As I enter I had a mail saying to jack that he needed to change the password because it was simple. With this information we can try hydra and try rockyou with this command `hydra -l jack -P rockyou.txt MACHINE_IP ssh` and gave me that the password is `987654321`. i went to ssh and try it and it entered. Now we navigate in the computer and we discover that the first answer to the first question is on `/home/holt`

Now we need to escalate priviliges, first I did `sudo -l` and found out that we can do the command `less` with `sudo`, so we exploit this vuleravility. In orden to do that we need to so `sudo less /etc/profile` and write the next command `!/bin/sh`. With that we are in as root so we navigate some more and find the answer to the second question

## Conclusion

It was not difficult, I had experience with ftp and escalating privileges was not as difficult as other challenges.