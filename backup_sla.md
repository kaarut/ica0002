<h1>[Backup coverage]</h1>

Services that are being backed up:
+ MySQL (Data only)
+ InfluxDB (Data only)
+ Ansible repository - https://github.com/kaarut/ica0002 (Full repo)

Everything else is not being backed up.

<h1>[Backup RPO]</h1>
The RPO is the acceptable amount of data that can be lost in the event of a failure. For example, if backups are taken once a day, then at most 24 hours of data will be lost if the system fails immediately before a regularly scheduled backup.

Backup recovery point objective:
+ MySQL = 12 hours
+ InfluxDB = 12 hours
+ Ansible repository = 12 hours

<h1>Versioning and retention</h1>
MySQL and Grafana backups are retained for 4 weeks/28 days, only 2 versions can be stored at the same time.

<h1>Usability checks</h1>
Restore the service to the test environment at any time.
Validate that restored data is shown in the service.

<h1>Restoration criteria</h1>
Restore the service from the backup to the desired state once per week.

<h1>[Backup RTO]</h1>

Backup recovery time objective:

Backup service is expected to take maximum of 1 hours to fully recover all the data. If the whole infrastructures should be restored, excepted maximum required time equals 2 hours.
