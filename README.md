# nmapList
List of useful nmap examples

Exhaustive Scan:
nmap -sV -n -v -Pn -p- -A --reason -oN nmap.txt $IP

SSL Strength Check:
nmap -Pn --script ssl-enum-ciphers -p 443 $HOSTNAME

Show Allowed HTTP Methods:
nmap -p 80 --script http-methods $IP