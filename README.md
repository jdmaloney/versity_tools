# Versity Tools

## ScoutFS Metadata Backup
Script that runs a dump of the scoutfs file system metadata.  This will allow for a restore of data from tape in the event that the file system has a catastrophic failure. Data that had been staged to tape will be able to be located with the data in this dump.

This script dumps the metadata at a pre-defined location, logs its activty, and sends a summary of metrics about the dump to an InfluxDB server.  It however is *NOT* run by telegraf; run this script via cron at an appropriate interval for your environment.
