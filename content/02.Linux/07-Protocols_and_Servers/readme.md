# Protocols and servers

## Goals  

1. HTTP/HTTPS
    - Configure a virtual host
    - Deploy a one pager 
2. SSH 
    - Configure key-based authentication
3. SMB
    - Provide network shares to specific clients
4. TELENET
    - Install and configuration
5. FTP
    - Install and configuration


## HTTP, FTP, SMTP, POP3, IMAP, SMB.

First, please follow tthese pdf :
- http://dma.vgtu.lt/KTA/KTA10_EN.pdf

## Exercises

> Connect to the virtual machine 10.12.181.X with the following credentials:  
> * ip : 10.12.181.X  
> * user : student  
> * password : student  

1.  On your kali (or other) , install ``ngnix`` to have an http server on port 8080. Replace the default page of ngnix by an html page displaying a hello world.
    > No answer required

1. What other well-known service could be used instead of nginx? 
    > Your answer :

1. On your student machine, create a temporary http server with python, on port ``5000``. Then on your kali machine, open a browser and go to the address ``10.12.181.X:``.
    > Your command : 

1. Let's imagine that a hacker owns the domain name ``g00gle.com``, which tool would allow him to obtain an ssl certificate (https) very easily?
    > Your answer :

1. On a linux machine, what tool could you use to have a self-signed SSL certificate on your local machine (localhost) ? 
    > Your answer : 

1. On your student machine, install the ftp service and connect from your kali machine.
    > No answer required

1. What is the default port for ftp? 
    > Your answer :

1. Is the ftp protocol secured?
    > Your answer :

1. On your student machine, install the telnet service and connect from your kali machine.
    > No answer required

1. What is the default port for telnet? 
    > Your answer :

1. Is the telnet protocol secured?
    > Your anbswer :
    
1. Create a share file with samba between your Kali machine and your student machine.
    > No answer required






