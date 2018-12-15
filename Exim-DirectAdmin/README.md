# Statistiques Exim pour Zabbix avec un server DirectAdmin

## Installation
```bash
yum -y install curl zabbix-sender logcheck
mkdir /etc/zabbix/scripts
cd /etc/zabbix/scripts/
wget https://github.com/webalternative/Zabbix/raw/master/Exim-DirectAdmin/da-eximstats.sh
chmod +x /etc/zabbix/scripts/da-eximstats.sh

### Ajouter la tâche CRON
*/5 * * * *  /etc/zabbix/scripts/da-eximstats.sh > /tmp/exim_zabbix.log

### Templates
Télécharger et importer les templates dans Zabbix

```

## Crédits
Script de base: https://gist.github.com/crashdump/5697771
