<properties
	pageTitle="Azure virtual machine backup monitoring and reporting issues"
	description="Azure virtual machine backup monitoring and reporting issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	displayOrder="5"
	selfHelpType="generic"
	supportTopicIds="32553291"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="7786d3f4-48b4-459f-8d12-d3f27e0e7cdd"
	ownershipId="StorageMediaEdge_Backup"
/>


# Azure virtual machine backup monitoring and reporting issues

## **Recommended steps**

**Note:** From 1st November, 2018, some customers may see issues in loading the data in Azure Backup App in Power BI, saying “We found extra characters at the end of JSON input. The exception was raised by the IDataReader interface.” This is due to a change in the format in which data is loaded into the storage account.

Please upgrade the App to the latest version to avoid facing the issue using [link](https://docs.microsoft.com/azure/backup/backup-azure-configure-reports#view-reports-in-power-bi)<br>

Try the recommended steps below to resolve common issues with Azure IaaS VM Backup monitoring and reporting:

* Note that alerts are raised only for failed backups

* If the email did not reach your inbox, please check in the spam or junk folders

* Are there situations where email isn't sent even if notifications are configured? Below are situations where an alert is not raised and email is not sent to reduce alert-noise<br>
	1. If notifications are configured to Hourly Digest, and an alert is raised and resolved within the hour <br>
	2. The job is canceled <br>
	3. A backup job is triggered and then fails, and another backup job is in progress <br>
	4. A scheduled backup job for a Resource Manager-enabled VM starts, but the VM no longer exists <br>

## **Recommended documents**

 [Azure virtual machine backup monitoring guide](https://azure.microsoft.com/documentation/articles/backup-azure-monitor-vms/)<br>
