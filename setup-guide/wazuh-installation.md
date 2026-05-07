# \# Wazuh Installation Guide



## \## Update System



```bash

sudo apt update \&\& sudo apt upgrade -y



### Install Wazuh

curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh

sudo bash ./wazuh-install.sh -a



### Access Dashboard

Open browser:

https://<WAZUH-IP>



### Default Credentials

Username: admin

Password: admin



### Install Wazuh Agent

curl -so wazuh-agent.deb https://packages.wazuh.com/4.x/apt/pool/main/w/wazuhagent/wazuh-agent\_4.7.0-1\_amd64.deb

sudo WAZUH\_MANAGER='<MANAGER-IP>' dpkg -i ./wazuh-agent.deb



### Start Agent

sudo systemctl daemon-reload

sudo systemctl enable wazuh-agent

sudo systemctl start wazuh-agent



