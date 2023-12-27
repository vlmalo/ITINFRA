# Backup SLA

### Backup Coverage
- What is backed up:
  - MySQL databse
  - InfluxDB database

### RPO (Recovery Point Objective)

## MySQL
- Full backups are done at 22:45 UTC
- Incremental backups are done at 22:45 UTC on every day-of-week from Monday through Saturday

## InfluxDB
- Full backups are done at 22:45 UTC
- Incremental backups are done at 22:45 UTC on every day-of-week from Monday through Saturday

### Versioning and Retention
- Full backups contain all data from services that are backed up. (done daily)
- Incremental backups retain difference from the last created backups.
- Retention period: 4 weeks.
- Only 28 versions of backups can be stored at the same time.
- Backups that are older than 29 days are deleted.

### Restoration Criteria
- Backup should be restored in case of:
  - Data corruption or loss.
  - Accidental deletion of critical data.
  - Database server failure.

### Backup Procedures
- Instructions are located in backup_restore.md

### RTO (Recovery Time Objective)
- Time to restore: Within 2 hours.

