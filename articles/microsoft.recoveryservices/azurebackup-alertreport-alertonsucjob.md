<properties
	pageTitle="Alert- How to configure on succeeded jobs"
	description="How to configure Alert on succeeded jobs"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632778"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
	articleId="d433e690-46fd-4792-98f7-628a6938e222"
/>

# Email notification on succeeded backup jobs

## **Recommended steps**

How to configure email notification on succeeded backup jobs?

**Note** : Alerts are designed for failure scenarios, currently there is NO support for notification on successful backups.<br>
  - For Azure virtual machine successful backup, a workaround is to use activity logs to get notifications. [See here for details](https://docs.microsoft.com/azure/backup/backup-azure-monitor-vms#using-activity-logs-to-get-notifications-for-successful-backups).<br>
  - MARS agent (files & Folder backup) does not support notification on successful backups and there are NO recommended workarounds.
