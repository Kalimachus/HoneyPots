# HoneyPots


1) Ubuntu - Dionaea with HTTP
NAME            ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP    STATUS
mhn-honeypot-1  us-central1-c  f1-micro                   10.128.0.2   35.188.62.181  RUNNING
wget "http://35.184.54.18/api/script/?text=true&script_id=4" -O deploy.sh && sudo bash deploy.sh http://35.184.54.18 9lEvuK62
Used NMAP, found openings.
Discovered scans from others across globe.
(https://imgur.com/4RsWcq9.png)

2) Ubuntu - Wordpot
NAME            ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP     STATUS
mhn-honeypot-2  us-central1-c  f1-micro                   10.128.0.4   35.192.189.158  RUNNING
wget "http://35.184.54.18/api/script/?text=true&script_id=17" -O deploy.sh && sudo bash deploy.sh http://35.184.54.18 9lEvuK62
Unable to access wordpress page.
Wordpot was not showing any processes for listening. Used Nikto and was able to detect other information:

+ Server: Apache/2.2.22 (Ubuntu)
+ The anti-clickjacking X-Frame-Options header is not present.
+ The X-XSS-Protection header is not defined. This header can hint to the user agent to protect against some forms of XSS
+ The X-Content-Type-Options header is not set. This could allow the user agent to render the content of the site in a different fashion to the MIME type
+ No CGI Directories found (use '-C all' to force check all possible dirs)
+ Apache/2.2.22 appears to be outdated (current is at least Apache/2.4.12). Apache 2.0.65 (final release) and 2.2.29 are also current.
+ Allowed HTTP Methods: HEAD, GET, POST, OPTIONS 

However, no attacks were detected.
Reference of instructions: https://itandsecuritystuffs.wordpress.com/2015/02/03/honeypot-networks/#more-316

3)Suricata
NAME            ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP   STATUS
mhn-honeypot-3  us-central1-c  f1-micro                   10.128.0.5   35.188.34.13  RUNNING
wget "http://35.184.54.18/api/script/?text=true&script_id=13" -O deploy.sh && sudo bash deploy.sh http://35.184.54.18 9lEvuK62
Unable to detect nmap scan. Host was not detected with Nikto.

4) Glastopf
NAME            ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP     STATUS
mhn-honeypot-4  us-central1-c  f1-micro                   10.128.0.6   35.192.189.158  RUNNING
wget "http://35.184.54.18/api/script/?text=true&script_id=8" -O deploy.sh && sudo bash deploy.sh http://35.184.54.18 9lEvuK62
Used NMAP, was silent. Used Nikto and was noisy.


5)Elastic Honey
NAME            ZONE           MACHINE_TYPE  PREEMPTIBLE  INTERNAL_IP  EXTERNAL_IP    STATUS
mhn-honeypot-5  us-central1-c  f1-micro                   10.128.0.7   35.188.195.86  RUNNING
Not able to connect to Host.
