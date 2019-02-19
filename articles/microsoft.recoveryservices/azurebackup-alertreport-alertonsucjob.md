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

## **Recommended Steps**

**Note**: Alerts are designed for failure scenarios. Currently there is NO support for notification on successful backups.<br>

  - For Azure Virtual Machine backups, you can [use activity logs to get notifications as a workaround](https://docs.microsoft.com/azure/backup/backup-azure-monitor-vms#using-activity-logs-to-get-notifications-for-successful-backups)
  - MARS agent (files & folder backup) does not support notification on successful backups, and there are no recommended workarounds
