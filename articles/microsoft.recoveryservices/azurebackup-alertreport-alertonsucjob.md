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

## **Recommended Documents**

- [How to create Alerts using Log Analytics?](https://aka.ms/Create-Alert-LA)
- [How to configure notifications for Alerts generated using Log Analytics?](https://aka.ms/BKP-LA-Notification)
- To configure Alert and Notification on successful backup jobs use query [all successful backup jobs](https://aka.ms/BKP-Alerts-AllSuccessfulJobs) while defining [alert condition](https://aka.ms/backup-Alert-condition) in Log Analytics <br>
- You can also use [Activity Logs](https://aka.ms/Configure-AlertsNotification-ActivityLogs) to get notifications for events such as backup success for Azure VMs, read [recommendations](https://aka.ms/BKP-Notification-Recommendations) before configuring notification using Activity Logs

**Note:** Log Analytics currently supports Azure VM backups, MAB Agent and System Center DPM, for more information read [note](https://aka.ms/Create-Alert-LA)
