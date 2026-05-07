# \# SSH Brute Force Detection Report

### \## Objective

The objective of this lab is to detect SSH brute force attacks using Wazuh SIEM.

\---

#### \## Attack Simulation

```bash

for i in {1..10}; do ssh fakeuser@<TARGET-IP>; done



##### Detection Rule

The Wazuh custom rule monitors failed SSH login attempts.



##### Alert Generated

Wazuh generated a high-severity alert after detecting multiple failed SSH login attempts.

##### 

##### MITRE ATT\\\\\\\\\\\\\\\&CK Mapping

T1110 — Brute Force



##### Impact

Successful brute force attacks can result in unauthorized system access.



##### Recommendations

Enable MFA

Use strong passwords

Disable root login

Restrict SSH access



##### Conclusion

The lab successfully demonstrated SSH brute force detection using Wazuh.

\\\\\\\\---



##### \\\\\\\\# reports/nmap-detection-report.md

```markdown

\\\\\\\\# Nmap Scan Detection Report

\\\\\\\\## Objective

The objective of this lab is to detect reconnaissance activity generated using

Nmap.

\\\\\\\\---

\\\\\\\\## Attack Simulation

```bash

nmap -sS <TARGET-IP>



##### Detection Rule

The Wazuh custom rule monitors Nmap scan activity from Suricata alerts.



##### Alert Generated

Wazuh successfully generated alerts for network reconnaissance activity.



##### MITRE ATT\\\\\\\\\\\\\\\&CK Mapping

T1046 — Network Service Discovery



##### Impact

Reconnaissance scanning helps attackers identify vulnerable services and open ports.



##### Recommendations

Close unused ports

Use firewall filtering

Monitor network traffic continuously



##### Conclusion

The lab successfully demonstrated detection of Nmap reconnaissance activity.

\\\\\\\\---

\\\\\\\\# attack-simulation/attack-commands.md

```markdown

\\\\\\\\# Attack Simulation Commands

\\\\\\\\## SSH Brute Force

```bash

for i in {1..10}; do ssh fakeuser@<TARGET-IP>; done



##### Hydra Brute Force

hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://<TARGET-IP>



##### Nmap SYN Scan

nmap -sS <TARGET-IP>



##### Aggressive Nmap Scan

nmap -A <TARGET-IP>





---

===


