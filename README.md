This is a modification of the original krb5-enum-users NMAP script. This version simply prints the username once it is discovered.
Have you found the old version frustrating because you are using a large username list and have to wait?

To start using this script, copy this script to your NMAP script directory. Then run the following two commands if you are using KALI:

└─$ sudo cp krb5-enum-users-hoichi.nse /usr/share/nmap/scripts
└─$ sudo nmap --script-updatedb

As an example of using this script (using TryHackMe's Attacktive box):

└─$ nmap -p 88 --script=krb5-enum-users-hoichi.nse --script-args krb5-enum-users-hoichi.realm='THM-AD',userdb=userlist.txt 10.10.210.178
