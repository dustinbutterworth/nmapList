# nmapList
List of useful nmap examples

Ping Scan (using cidr)
```
nmap -sn -n 10.100.13.0/24
```

Exhaustive Scan:
```
nmap -sV -n -v -Pn -p- -A --reason -oN nmap.txt $IP
```

SSL Strength Check:
```
nmap -Pn --script ssl-enum-ciphers -p 443 $HOSTNAME
```

SSH Cipher Check:
```
nmap --script=ssh2-enum-algos.nse -n -PS22 -p22 $IP
```

Show Allowed HTTP Methods:
```
nmap -p 80 --script http-methods $IP
```

Nmap against multiple hosts:
```
nmap -n -PS22 -p22 -iL hosts
```

Don't forget the nifty vulners script:
--script vulners
