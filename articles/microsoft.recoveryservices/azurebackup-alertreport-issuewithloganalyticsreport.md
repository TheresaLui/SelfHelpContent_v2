<properties
	pageTitle="Reports - issues with Log Analytics report"
	description="Issues with Log Analytics report"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632788"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7860bb83-8a94-4d43-acf9-6f48167fcf4e"
	ownershipId="StorageMediaEdge_Backup"
/>

# Issues with Log Analytics report

## **Recommended Steps**

- To configure backup reports, [follow these instructions](https://docs.microsoft.com/azure/backup/configure-reports) 
- To configure diagnostics settings at scale for your vaults, [follow these instructions](https://docs.microsoft.com/azure/backup/azure-policy-configure-diagnostics)
 
**Basic troubleshooting steps**
- Ensure that you have selected all of the required diagnostics events and the correct value in the toggle. [Learn more](https://docs.microsoft.com/azure/backup/backup-azure-diagnostic-events)
- Ensure that the retention of your Log Analytics (LA) workspace is sufficient. You can navigate to the LA workspace to update its retention. [Learn more](https://docs.microsoft.com/azure/backup/configure-reports#1-create-a-log-analytics-workspace-or-use-an-existing-one)
- Note that: 
  - For **DPM workloads**, Backup reports are supported for **DPM Version 5.1.363.0 and above** and **Agent Version 2.0.9127.0 and above**
  - For **MABS workloads**, Backup reports are supported for **MABS Version 13.0.415.0 and above** and **Agent Version 2.0.9170.0 and above**

## **Recommended Documents**

**Monitor backup Jobs and create Alerts/Notifications using Log Analytics**<br>

Log Analytics currently supports Azure VM backups, MAB Agent, and System Center DPM. For more information, refer to this [article](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics).

- [Create alerts using Log Analytics](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics)
- [Configure notifications for alerts generated using Log Analytics](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#create-alerts-by-using-log-analytics)
- [Monitor Azure Backup using Log Analytics](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#using-log-analytics-workspace)
- [What is the data pumping frequency to Log Analytics?](https://docs.microsoft.com/azure/backup/backup-azure-monitoring-use-azuremonitor#diagnostic-data-update-frequency)<br>

