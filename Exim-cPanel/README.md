# Statistiques Exim pour Zabbix avec un server cPanel

## Installation
```bash
yum -y install curl zabbix-sender logcheck
mkdir /etc/zabbix/scripts
cd /etc/zabbix/scripts/
wget https://github.com/webalternative/Zabbix/raw/master/Exim-cPanel/cpanel-eximstats.sh
chmod +x /etc/zabbix/scripts/cpanel-eximstats.sh
```
### Ajouter la tâche CRON
*/5 * * * *  /etc/zabbix/scripts/cpanel-eximstats.sh > /tmp/exim_zabbix.log

### Templates
Télécharger et importer les templates dans Zabbix

### Firewall
Ouvrir le port 10051 pour permettre l'envois d'informations à partir du zabbix-sender


## Crédits
Script de base: https://gist.github.com/crashdump/5697771
