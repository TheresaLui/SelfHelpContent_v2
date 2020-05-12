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
	cloudEnvironments="MoonCake"
	articleId="fd89fe97-213e-4abc-a695-9e7d347db5c6"
	ownershipId="StorageMediaEdge_Backup"
/>


# Azure virtual machine backup monitoring and reporting issues

## **Recommended steps**
Try the recommended steps below to resolve common issues with Azure IaaS VM Backup monitoring and reporting

* Note that alerts are raised only for failed backups

* If the email did not reach your inbox, please check in the spam or junk folders

* Are there situations where email isn't sent even if notifications are configured? Below are situations where an alert is not raised and email is not sent to reduce alert-noise<br>
	1. If notifications are configured to Hourly Digest, and an alert is raised and resolved within the hour <br>
	2. The job is canceled <br>
	3. A backup job is triggered and then fails, and another backup job is in progress <br>
	4. A scheduled backup job for a Resource Manager-enabled VM starts, but the VM no longer exists <br>

##**Recommended documents**

 [Azure virtual machine backup monitoring guide](https://docs.azure.cn/backup/backup-azure-monitor-vms)<br>
