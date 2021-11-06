<h1>[Infra]</h1>

Install and configure infrastructure with Ansible:

    ansible-playbook infra.yaml

<h3>[How to restore MYSQL?]</h3>

Restore MySQL data from the backup:

    sudo -u backup duplicity --no-encryption restore rsync://kaarut@backup//home/kaarut/ /home/backup/restore/agama.sql

    sudo mysqldump agama < /home/backup/restore/agama.sql 

<h3>[How to restore InfluxDB?]</h3>

Restore InfluxDB data from the backup:
     
    service telegraf stop
    influx -execute 'DROP DATABASE telegraf'

    [RESTORE LOCAL BACKUP]
    influxd restore -portable -database telegraf /home/backup/influxdb

    [IF THE LOCAL BACKUP WAS CORRUPTED]
    sudo -u backup duplicity --no-encryption restore rsync://kaarut@backup//home/kaarut/ /home/backup/restore/
    influxd restore -portable -database telegraf /home/backup/restore   



