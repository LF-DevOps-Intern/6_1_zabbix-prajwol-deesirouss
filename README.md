# 6_1_ZABBIX-Prajwol
## [Assignment's Full PDF Answer with ScreenShots](https://github.com/LF-DevOps-Intern/6_1_zabbix-prajwol-deesirouss/blob/main/Zabbix-answer-PDF.pdf)

Assignment for Zabbix on Week 6 - Day 1

Tasks:
1. Install Zabbix Server 5 on VM that includes:
- Zabbix Server
- Database
- Apache
- PHP
- Zabbix Server-Modules for Apache & Database
- Zabbix Frontend
## [Task-1's Answer with ScreenShots](https://github.com/LF-DevOps-Intern/6_1_zabbix-prajwol-deesirouss/blob/main/1/1-Install-Zabbix.pdf)

2. Provide screenshot of
- Running Zabbix Server service,
- Database config parameter in server config file
- Server Dashboard
## [Task-2's ScreenShots](https://github.com/LF-DevOps-Intern/6_1_zabbix-prajwol-deesirouss/blob/main/2/2-ScreenShot.pdf)


3. Install Latest Zabbix Agent on VM or host machine or server itself to fetch logs, steps include:
- Run as active check agent
- Add a logging item to the same template for fetching /var/log/syslog(Ubuntu) or /var/log/messages
(CentOS)
- Fetch those logs from the host (Make sure required permissions are set for zabbix-agent to
pull logs)
- Provide agent configuration file & screenshots for target machine graph & logs
## [Task-3's Answer with ScreenShots](https://github.com/LF-DevOps-Intern/6_1_zabbix-prajwol-deesirouss/blob/main/3/3-zabbix-agent.pdf)
### [agent configuration file](https://github.com/LF-DevOps-Intern/6_1_zabbix-prajwol-deesirouss/blob/main/3/zabbix_agentd.conf)
* Please check shared slides for any reference *


Sample agent config for passive checks on Ubuntu
# File for process id
PidFile=/run/zabbix/zabbix_agentd.pid
# Zabbix agent log location
LogFile=/var/log/zabbix-agent/zabbix_agentd.log
# Maximum size of log file, 0 disables automatic log rotation
LogFileSize=0
# Server for Passive check
Server=$SERVER
# Server for Active check
#Server=$SERVER
#Preforked instance of zabbix agent for passive check, 0 for active checks
StartAgents=2
#Device Hostname
Hostname=$HOSTNAME
# Get all metadata from uname
HostMetadataItem=system.uname# How agent connects to server
TLSConnect=unencrypted
# How incoming connections are accepted
TLSAccept=unencrypted
# PSK Identity string
#TLSPSKIdentity=$PSK_NAME
# Location of PSK
#TLSPSKFile=$PSK_PATH
