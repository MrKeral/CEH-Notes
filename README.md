# CEH-Notes

> sudo netdiscover -r 192.168.1.0/24				
## NMAP
> Best <br/>
> nmap -A -T4 -p- 192.168.1.0/24 <br/>
> nmap -sC -sV -Pn -T4 -vv -p- 192.168.1.0/24 <br/>
> nmap --script vuln -Pn -T4 -p- 192.168.1.0/24 <br/>
> <br/>
> Firewall/IDS, if opened <br/>
> nmap -sS -v -p- 192.168.1.0/24  <br/>
> nmap -f -p- 192.168.1.0/24 <br/>
> <br/>
> UDP Scan <br/>
> nmap -sU --top-ports 25 -p- 192.168.1.0/24 <br/>

## WP SCAN <br/>
> wpscan --url http://192.168.0.1 <br/>
> wpscan --url http://192.168.0.1 -e u    #User Enum <br/>
> wpscan --url http://192.168.0.1 --enumerate u <br/>
> wpscan --url http://192.168.0.1 --usernames /home/user.txt --passwords /home/pass.txt  <br/>
> wpscan --url http://192.168.0.1 -u john --passwords /home/pass.txt  <br/>

## METASPLOIT <br/>
> msfconsole : <br/>
> use auxilliary/scanner/http/wordpress_login_enum <br/>
> show options <br/>
>	set PASS_FILE /home/attacker/Desktop/Wordlist/password.txt <br/>
>	set RHOSTS 10.10.10.10  (target ip) <br/>
>	set RPORT 8080          (target port) <br/>
>	set TARGETURI http://10.10.10.10:8080/ <br/>
>	set USERNAME admin <br/>
> 
 
