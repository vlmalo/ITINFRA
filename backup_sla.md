# Backup SLA

## Database Servers

### Backup Coverage
- What is backed up: Full database dumps, including schema and data.
- What is not backed up: Temporary files, cache.

### RPO (Recovery Point Objective)
- Desired data loss: Within the last 24 hours.

### Versioning and Retention
- Number of backup versions: 7.
- Retention period: 30 days.

### Usability Checks
- Verification through automated scripts checking the integrity of backup files.
- Regular restore tests to a non-production environment.

### Restoration Criteria
- Backup should be restored in case of:
  - Data corruption or loss.
  - Accidental deletion of critical data.
  - Database server failure.

### RTO (Recovery Time Objective)
- Time to restore: Within 2 hours.

## InfluxDB

### Backup Coverage
- What is backed up: InfluxDB data directory.
- What is not backed up: Temporary files, InfluxDB cache.

### RPO (Recovery Point Objective)
- Desired data loss: Within the last 12 hours.

### Versioning and Retention
- Number of backup versions: 5.
- Retention period: 15 days.

### Usability Checks
- Verification through InfluxDB's built-in integrity checks.
- Regular restore tests to a non-production environment.

### Restoration Criteria
- Backup should be restored in case of:
  - Data corruption or loss.
  - InfluxDB server failure.

### RTO (Recovery Time Objective)
- Time to restore: Within 1 hour.

## Ansible Repository

### Backup Coverage
- What is backed up: Ansible playbooks, roles, inventories.
- What is not backed up: Temporary files, cache.

### RPO (Recovery Point Objective)
- Desired data loss: Within the last 24 hours.

### Versioning and Retention
- Number of backup versions: 10.
- Retention period: 30 days.

### Usability Checks
- Verification through automated playbook runs on a non-production environment.
- Regular restore tests to a non-production environment.

### Restoration Criteria
- Backup should be restored in case of:
  - Loss of critical playbooks or roles.
  - Unauthorized changes to the Ansible repository.

### RTO (Recovery Time Objective)
- Time to restore: Within 3 hours.

