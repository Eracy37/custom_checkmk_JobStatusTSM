# custom_checkmk_JobStatusTSM
Script for Job status Tivoli IBM - Compatibility AIX

### Prerequies

```bash
# Configuration is needed for username and password for dsmadmc
# You need to create a configuration file /etc/check_mk/tsm.cfg
# with the following two lines:
# TSM_USER=XXX
# TSM_PASSWORD=XXX
# If you have more than once instance, make sure that the upper
# login works on all of them.
```
Add the script in crontab so that it runs every 10 minutes

The script is slow, so you need to create another script to read the result of the script in ```/usr/lib/check_mk_agent/local```
File : result_check_job-TSM.txt

### Use

Checkmk agent do an inventory for result.
