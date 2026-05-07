# \# Lab Architecture



## \## Components



### \### Kali Linux



Used as the attacker machine to simulate cyberattacks.

#### \### Ubuntu Server



Used as the target machine where attacks are performed.

#### \### Wazuh Manager



Collects logs, analyzes events, and generates alerts.

#### \### Suricata IDS



Monitors suspicious network activity and intrusion attempts.

\---

##### \## Workflow

1\. Attacker machine launches attack.

2\. Ubuntu server generates logs.

3\. Wazuh agent forwards logs.

4\. Wazuh manager analyzes events.

5\. Alerts are generated on dashboard.

