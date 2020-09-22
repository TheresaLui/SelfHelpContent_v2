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
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d433e690-46fd-4792-98f7-628a6938e222"
	ownershipId="StorageMediaEdge_Backup"
/>

# Email notification on succeeded backup jobs

## **Recommended Documents**

- [Create alerts using Log Analytics](https://aka.ms/Create-Alert-LA)
- [Configure notifications for alerts generated using Log Analytics](https://aka.ms/BKP-LA-Notification)
- To configure alert and notification on successful backup jobs, use query [all successful backup jobs](https://aka.ms/BKP-Alerts-AllSuccessfulJobs) while defining [alert condition](https://aka.ms/backup-Alert-condition) in Log Analytics <br>
- You can also use [Activity Logs](https://aka.ms/Configure-AlertsNotification-ActivityLogs) to get notifications for events such as backup success for Azure VMs. Please read [recommendations](https://aka.ms/BKP-Notification-Recommendations) before configuring notification using Activity Logs.

**Note:** Log Analytics currently supports Azure VM backups, MAB Agent, and System Center DPM. For more information, refer to this [article](https://aka.ms/Create-Alert-LA).
