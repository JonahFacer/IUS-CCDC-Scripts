Link to login ccdcadmin3.morainevalley.edu





1) Changing users and admin passwords for the domain(active directory) and local device, LDAP + services
2) Disabling uneeded services/firewall restricting which network ranges can connect, Windows - SMB, WinRM, RDP, Netbios, etc. Linux - ssh, smb, ftp, print ports, etc.
3) Running hardening scripts to severely reduce exploitation potential.

# Windows:
https://github.com/atlantsecurity/windows-hardening-scripts/blob/main/Windows-10-Hardening-script.cmd
https://github.com/atlantsecurity/windows-hardening-scripts/blob/main/windows-server-2019-hardening-script.cmd

# Linux:
https://www.youtube.com/watch?v=XYxybI7xZTw
https://github.com/konstruktoid/hardening
https://github.com/4rji/ccdc (havent checked the safety of this yet)
https://github.com/CISOfy/Lynis (Well know linux security auditing tool).

4) Begin downloading security software on windows. (Antivirus/Firewall, Sysmon, Comodo Cleaning Essentials - Use the taskmanager and enable service+autorun logging, etc)
https://learn.microsoft.com/en-us/sysinternals/downloads/autoruns
https://learn.microsoft.com/en-us/sysinternals/downloads/sysmon
https://help.comodo.com/topic-119-1-328-3523-.html
https://antivirus.comodo.com/free-antivirus.php
https://www.zonealarm.com/software/free-firewall

5) Begin downloading security software for linux. Assuming the above automated hardening scripts werent used. (PSAD, RKHunter, chkrootkit, fail2ban, clamAV, tripwire, loki yara scanner, etc)
https://www.rapid7.com/blog/post/2017/06/24/how-to-install-and-use-psad-ids-on-ubuntu-linux/
https://www.webhi.com/how-to/how-to-install-and-configure-rootkit-hunter-on-ubuntu-debian/
https://www.alibabacloud.com/blog/how-to-install-chkrootkit-security-scanner-on-ubuntu-18-04_595711
https://www.liquidweb.com/blog/install-clamav/
https://www.secopsolution.com/blog/install-and-configure-fail2ban
https://docs.vultr.com/how-to-install-tripwire-intrusion-detection-system-on-debian-11
https://github.com/Neo23x0/Loki

6) Start hunting for pre-existing infections (using autoruns for windows, or chkrootkit/rkhunter on linux, webshells, malicious accounts, etc.
7) Harden system services that HAVE to remain active, do this while security tools, updates, etc are downloading in the background.

Linux MySQL: https://www.axcelsec.com/2018/06/web-server-hardening-mysql.html
Linux NTP: https://hackviser.com/tactics/hardening/ntp
Linux SSH: https://hackviser.com/tactics/hardening/ssh

Linux Webserver(apache): 
https://www.tecmint.com/apache-security-tips/
https://hackviser.com/tactics/hardening/apache

Linux Webserver(nginx) - Ignore the binary compilation part: 
https://help.dreamhost.com/hc/en-us/articles/222784068-The-most-important-steps-to-take-to-make-an-nginx-server-more-secure
https://hackviser.com/tactics/hardening/nginx

Linux Splunk: https://conf.splunk.com/files/2020/slides/TRU1537C.pdf
Linux Mailserver(postfix): https://linux-audit.com/postfix-hardening-guide-for-security-and-privacy/
Linux DNS(bind): 
https://kb.isc.org/docs/bind-best-practices-authoritative
https://kb.isc.org/docs/bind-best-practices-recursive
https://hackviser.com/tactics/hardening/bind9

Linux Docker:
https://cheatsheetseries.owasp.org/cheatsheets/Docker_Security_Cheat_Sheet.html
https://medium.com/@SecurityArchitect/hardening-container-images-best-practices-and-examples-for-docker-e941263cab13

General Linux Hardening:
https://linux-audit.com/system-hardening/guides/ubuntu/
https://madaidans-insecurities.github.io/guides/linux-hardening.html

General Windows Hardening:
https://www.cyber.gov.au/sites/default/files/2023-03/PROTECT%20-%20Hardening%20Microsoft%20Windows%2010%20version%2021H1%20Workstations%20%28October%202021%29.pdf

Windows (Active Directory): 
https://medium.com/@john245461/active-directory-hardening-c804f3c3e63e
https://www.youtube.com/watch?v=S9u6-rhJl8k
https://dl.dod.cyber.mil/wp-content/uploads/stigs/zip/U_MS_Windows_Server_2019_V3R2_STIG.zip
https://www.pingcastle.com/download/
