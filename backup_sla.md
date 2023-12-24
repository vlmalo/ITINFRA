# Backup SLA

### Backup Coverage
- What is backed up:
  - Web services
  - App services
  - Database services
  - DNS services
  - Grafana dashboards and exporters

### RPO (Recovery Point Objective)
- Daily backups.

### Versioning and Retention
- Timestamping.
- Retention period: 4 weeks.

### Restoration Criteria
- Backup should be restored in case of:
  - Data corruption or loss.
  - Accidental deletion of critical data.
  - Database server failure.

### Backup Procedures
- Instructions are located in backup_restore.md

### RTO (Recovery Time Objective)
- Time to restore: Within 2 hours.

