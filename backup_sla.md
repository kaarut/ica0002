<h1>[Backup coverage]</h1>

Services that are being backed up:
+ MySQL (Data only)
+ InfluxDB (Data only)
+ Ansible repository - https://github.com/kaarut/ica0002 (Full repo)

Everything else is not being backed up.

<h1>[Backup RPO]</h1>

Backup recovery point objective:
+ MySQL = 4 weeks / 28 days
+ InfluxDB = 4 weeks/  28 days
+ Ansible repository = 4 weeks / 28 days

<h1>Versioning and retention</h1>

<h1>Usability checks</h1>

<h1>Restoration criteria</h1>

<h1>[Backup RTO]</h1>

Backup recovery time objective:
Backup service is expected to take maximum of 1 hours to fully recover all the data. If the whole infrastructures should be restored, excepted maximum required time equals 2 hours.
