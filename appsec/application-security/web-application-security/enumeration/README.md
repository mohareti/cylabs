# Enumeration

Burpsuite

amass enum -passive -d dfwairport.com -o results.txt

sublist3r -d dfwairport.com

./scripts/ct.py example.com | ./bin/massdns -r ./lists/resolvers.txt -o S -w results.txt

true | openssl s\_client -connect dfwairport.com:443 2>/dev/null | openssl x509 -noout -text  | perl -l -0777 -ne '@names=/\bDNS:(\[^\s,]+)/g; print join("\n", sort @names);'

Grep domain names only

grep -oE '\[a-zA-Z0-9.-]+\\.com' \<file\_name>

Grep IP addresses only\
grep -oE '\[0-9]+\\.\[0-9]+\\.\[0-9]+\\.\[0-9]+' \<file\_name>

Unique items by count and descending order\
sort \<file\_name> | uniq -c | sort -nr

Remove duplicates\

sort \<file\_name> | uniq > \<output\_file>

 BugBounty/webapp/mobile app

Web app handbook

Real world bug hunting

Owasp testing guide

Bugbounty bootcamp

The hackers playbook 3

Breaking into information security

Hands on hacking

Bug bounty playbook 1 and 2

Try Hack me

Pentesterlab

Websecurity academy

Hackthebox

vulnub

Subscription to

HackerOne

BugCrowd

Cobalt

Synack

Integriti

Approach

* Asset discovery
* Scope
* Subdomain enumeration
  * Horizontal
  * Vertical
* Open ports and services
* Web hosting softwares, misconfigurations, exploits
* Application framework
* Application custom codes or cots
* Application libraries
* Integrations

Browser plugins

* wappalyzer
* whatruns
* Webanalyze : cli tools

Nuclie

Nuclei -l httprobe.txt -t brute-force/\* -t cves/\* -t basic-detections/\* -t dns/\* -t files/\* -t panels/\* -t security-misconfiguration/\* -t subdomain-takeover/\* -t technologies/\* -t tokes/\* -t vulnerabilities/\*

* Know vulnerabilities
* Framework logins
* Default creds

Jaeles scanner

Ritire.js

Vulners burp extension

Intrigue core

Sn1per by

Gofingerprint

Portscanning

Naabu

 contentdiscovery tools

* Trubointruder
* Gobuster
* Ffuf
* Dirsearch
* Wfuzz
* Feroxbuster
* Dirbuster

Wordlist and content discovery

* Wordlist.Assetnote.com
* Jhaddix content discovery all
* Robots disallowed
* RAFT
* Six2detonelistforall
* Jhaddix api-endpoints.txt
* Source2URL by danielmessier
* Scavenger 0xdexter0us
* Getallurls
* Wordlistgen
* Trashcompactor
* Do recursive scans
* Apkleaks
* Changedetection.io

Application testing

* How app stores and send the data
* How app identifies user

Spidering

* Zap
* Burp
* Gospider
* Hackrawler
* xlinkfinder

Subdomain Enumeration

Sunday, May 22, 2022

2:23 PM

sublist3r -d {domainName}

amass enum -d {domainName}

amass intel -org uber

From < <https://danielmiessler.com/study/amass/>>

 amass intel -d target.com -whois

amass enum -passive -d target.com -src

 amass enum -ip -d target.com

 amass viz -d3 -dir resultdirectory

amass db -dir target.com(directory) -list

amass intel -ip -src -cidr 104.154.0.0/15

amass viz -d3 domains.txt -o 443 /your/dir/

Amass -src -ip -config amass\_config.ini -d

Amass -asn

amass enum -d \<URL> -p 443,8080

amass enum -d \<URL1>,\<URL2> -active

From < <https://allabouttesting.org/owasp-amass-quick-tutorial-example-usage/>>

From < <https://allabouttesting.org/owasp-amass-quick-tutorial-example-usage/>>

subfinder -d {domainName}

python3 subbrute.py {domainName}

python knock.py {domainName}

gobuster dns -d tesla.com -w simple-subdomain-list.txt

curl -k -s “ <https://crt.sh/?q=tesla.com&output=json>" | jq -r ‘.\[] | “\\(.name\_value)\n\\(.common\_name)”’ | sort -u

curl -k -s  <https://sonar.omnisint.io/subdomains/tesla.com> | jq -r ‘.\[]’ | sort -u

ffuf -c -w /path/to/list -u  <https://tesla.com/FUZZ>

ffuf -c -w /path/to/curated.txt -u  <https://tesla.com/FUZZ>

Robots disallowed list

ffuf -c -w /path/to/directories.txt -u  <https://tesla.com/FUZZ>

Fuzzing get parameters and values

ffuf -c -w /path/to/parameters.txt -u  <https://target/script.php?FUZZ=test_value>

ffuf -c -w /path/to/parameters.txt -u  <https://target/script.php?valid_name=FUZZ>

Password spraying and rate limit

ffuf -c -w /path/to/passwords.txt -X POST -d “username=admin\\\&password=FUZZ“ -u  <https://target/login.php>

ffuf -w params.txt:PARAM -w values.txt:VAL -u  <https://example.org/?PARAM=VAL> -mr “VAL” -c

dnsvalidator -tL <https://public-dns.info/nameservers.txt> -threads 100 -o resolvers.txt

Copied!

## In this section

* ✅ [Cookie and Header Security Review](cookie-and-header-security-review.md)
