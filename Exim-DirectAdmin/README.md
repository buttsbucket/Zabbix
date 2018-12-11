# Statistiques Exim pour Zabbix avec un server DirectAdmin

## Installation

yum -y install curl zabbix-sender logcheck
mkdir /etc/zabbix/scripts
cd /etc/zabbix/scripts/
wget https://github.com/webalternative/Zabbix/raw/master/Exim-DirectAdmin/da-eximstats.sh
chmod +x /etc/zabbix/scripts/da-eximstats.sh >/dev/null 2>&1
crontab -e

*/5 * * * *  /etc/zabbix/scripts/da-eximstats.sh


