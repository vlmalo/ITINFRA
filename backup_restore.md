## Install and configure infrastructure with Ansible:

`ansible-playbook infra.yaml` 

## Restore MySql data from the backup

- `sudo -u backup duplicity --no-encryption restore rsync://vlmalo@backup.talkmate.it/mysql /home/backup/restore/mysql`
- `sudo su`
- `mysql agama < /home/backup/restore/mysql/agama.sql`

## Restore telegraf

- `sudo -u backup duplicity --no-encryption restore rsync://vlmalo@backup.talkmate.it/influxdb /home/backup/restore/influxdb`
- `sudo su`
- `service telegraf stop`
- `influx -execute 'DROP DATABASE telegraf'`
- `influxd restore -portable -database telegraf /home/backup/restore/influxdb`
- `sudo service telegraf start`
