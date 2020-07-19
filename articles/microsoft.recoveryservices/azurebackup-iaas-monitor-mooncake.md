<properties
	pageTitle="Azure virtual machine backup monitoring and reporting issues"
	description="Azure virtual machine backup monitoring and reporting issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	ms.author="saurse"
	displayOrder="21"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-iaas-monitor-mooncake"
	ownershipId="Compute_SiteRecovery"
/>


# Azure virtual machine backup monitoring and reporting issues

## **Recommended Steps**

**Note:** From 1st November, 2018, some customers may see issues in loading the data in Azure Backup App in Power BI, saying "We found extra characters at the end of JSON input. The exception was raised by the IDataReader interface." This is due to a change in the format in which data is loaded into the storage account.

Try the recommended steps below to resolve common issues with Azure IaaS VM Backup monitoring and reporting:

* Note that alerts are raised only for failed backups
* If the email did not reach your inbox, please check in the spam or junk folders
* Are there situations where email isn't sent even if notifications are configured? Below are situations where an alert is not raised and email is not sent to reduce alert-noiseL

	1. If notifications are configured to Hourly Digest, and an alert is raised and resolved within the hour
	2. The job is canceled
	3. A backup job is triggered and then fails, and another backup job is in progress
	4. A scheduled backup job for a Resource Manager-enabled VM starts, but the VM no longer exists

## **Recommended Documents**

* [Azure virtual machine backup monitoring guide](https://docs.azure.cn/backup/backup-azure-monitoring-built-in-monitor)
