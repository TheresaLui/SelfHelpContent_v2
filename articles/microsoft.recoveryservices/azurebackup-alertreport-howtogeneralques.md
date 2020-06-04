<properties
	pageTitle="Alert and Report How-to and general questions"
	description="How-to and general questions"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632779"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="087eebee-9f42-4589-97f7-982e582dd0a3"
	ownershipId="StorageMediaEdge_Backup"
/>

# Alert and Report How-to and general questions

## **Recommended Steps**

- To configure alert and notification on successful backup jobs use query [all successful backup jobs](https://aka.ms/BKP-Alerts-AllSuccessfulJobs) while defining [alert condition](https://aka.ms/backup-Alert-condition) in Log Analytics <br>
- You can also use [Activity Logs](https://aka.ms/Configure-AlertsNotification-ActivityLogs) to get notifications for events such as backup success for Azure VMs. Please read [recommendations](https://aka.ms/BKP-Notification-Recommendations) before configuring notification using Activity Logs

## **Recommended Documents**

**Azure Backup Monitoring and Reporting using Power BI**

- [Configure backup report using Power BI](https://aka.ms/AB-backupReorts)
- [Supported scenarios](https://aka.ms/BKP-PowerBIReport-SupportedScenarios) and [prerequisites](https://aka.ms/BKP-PowerBIReport-Prerequisites) to configure Azure Backup Power BI report
- [View backup reports in Power BI](https://aka.ms/View-PowerBI-Report)
- [Frequently asked questions for Power BI reporting](https://aka.ms/BKP-PowerBIReport-FAQs)
- [Common issues while configuring Azure Backup Power BI report](https://aka.ms/BKP-PowerBIReport-Tshooting)

**Monitor backup Jobs and Alerts in Recovery Services vault**

- [Monitor Azure Backup Jobs in Recovery Services vault](https://aka.ms/Monitor-JobsAlert-RSV)
- [Monitor Backup Alerts in Recovery Services vault](https://aka.ms/AB-AA4e56k)
- [What are the scenarios where Backup Alerts are generated?](https://aka.ms/BKP-RSVAlert-Scenarios)
- [What are the exceptions when a Backup Alert is not raised on backup failure?](https://aka.ms/BKP-RSVAlert-Exceptions)
- [Azure Backup solutions for which Backup Alerts can be monitored in Recovery Services vault](https://aka.ms/BKP-RSVAlert-SupportedSolutions)
- [What types of Backup Alerts are available in Recovery Services vault?](https://aka.ms/RSV-Alert-Types)
- [Configure email notifications for Backup Alerts through Recovery Services vault](https://aka.ms/Configure-Notification-RSV)

**Monitor backup Jobs and create Alerts/Notifications using Log Analytics**<br>

Log Analytics currently supports Azure VM backups, MAB Agent, and System Center DPM. For more information, refer to this [article](https://aka.ms/Create-Alert-LA).

- [Create alerts using Log Analytics](https://aka.ms/Create-Alert-LA)
- [Configure notifications for alerts generated using Log Analytics](https://aka.ms/BKP-LA-Notification)
- [Monitor Azure Backup using Log Analytics](https://aka.ms/Monitor-Backup-LA)
- [Data pumping frequency to Log Analytics](https://aka.ms/BKP-LA-DataFrequency)<br>
