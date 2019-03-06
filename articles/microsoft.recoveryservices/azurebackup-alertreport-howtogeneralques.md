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
	cloudEnvironments="public"
	articleId="087eebee-9f42-4589-97f7-982e582dd0a3"
/>

# Alert and Report How-to and general questions

## **Recommended Documentation**

**Azure Backup Monitoring and Reporting using Power BI**

- [How to configure Backup report using Power BI?](https://aka.ms/AB-backupReorts)
- What are the [Supported Scenarios](https://aka.ms/BKP-PowerBIReport-SupportedScenarios) and [Prerequisites](https://aka.ms/BKP-PowerBIReport-Prerequisites) to configure Azure Backup Power BI report?
- [How to view backup reports in Power BI?](https://aka.ms/View-PowerBI-Report)
- [Frequently Asked Questions for Power BI reporting](https://aka.ms/BKP-PowerBIReport-FAQs)
- [Common issues while configuring Azure Backup Power BI report](https://aka.ms/BKP-PowerBIReport-Tshooting)

**Monitor backup Jobs and Alerts in Recovery Service Vault**

- [How to monitor Azure Backup Jobs in Recovery Service Vault?](https://aka.ms/Monitor-JobsAlert-RSV)
- [How to monitor Backup Alerts in Recovery Service Vault?](https://aka.ms/AB-AA4e56k)
- [What are the scenarios where Alerts are generated?](https://aka.ms/BKP-RSVAlert-Scenarios)
- [What are the exceptions when an alert is not raised on backup failure?](https://aka.ms/BKP-RSVAlert-Exceptions)
- [For which Azure Backup solutions Alerts can be monitor in Recovery Service Vault?](https://aka.ms/BKP-RSVAlert-SupportedSolutions)
- [What types of Alerts are available in Recovery Service Vault?](https://aka.ms/RSV-Alert-Types)
- [How to configure E-mail notifications for Backup Alerts through Recovery Service Vault?](https://aka.ms/Configure-Notification-RSV)

**Monitor backup Jobs and Create Alerts/Notifications using Log Analytics**

- [How to create Alerts using Log Analytics?](https://aka.ms/Create-Alert-LA)
- [How to configure notifications for Alerts generated using Log Analytics?](https://aka.ms/BKP-LA-Notification)
- [How to monitor Azure Backup using Log Analytics?](https://aka.ms/Monitor-Backup-LA)
- [What is the data pumping frequency to Log Analytics?](https://aka.ms/BKP-LA-DataFrequency)

**Recommendations**

- To configure Alert/Notification on successful backup jobs use query [all successful Azure VMs backup jobs](https://aka.ms/Successful-BackupAlert-IAASVM) while defining [alert condition](https://aka.ms/backup-Alert-condition) in Log Analytics <br>
- You can also use [Activity Logs](https://aka.ms/Configure-AlertsNotification-ActivityLogs) to get notifications for events such as backup success but read [Recommendations](https://aka.ms/BKP-Notification-Recommendations) before configuring notification using Activity Logs
