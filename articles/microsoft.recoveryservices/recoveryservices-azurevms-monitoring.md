<properties
	pageTitle="Azure IaaS VM Backup monitoring and reporting issues"
	description="Azure IaaS VM Backup monitoring and reporting issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="saurabhsensharma"
	displayOrder=""
	selfHelpType="resource"
	supportTopicIds="32447361"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public"
/>


# Azure IaaS VM Backup monitoring and reporting issues

## **Recommended steps**
Try the recommended steps below to resolve common issues with Azure IaaS VM Backup monitoring and reporting<br>
* Note that alerts are raised only for failed backups.
* If the email did not reach your inbox, please check in the spam or junk folders.
* Are there situations where email isn't sent even if notifications are configured? Below are situations where an alert is not raised and email is not sent to reduce alert-noise.<br>
    - If notifications are configured to Hourly Digest, and an alert is raised and resolved within the hour
    - The job is canceled
    - A backup job is triggered and then fails, and another backup job is in progress
    - A scheduled backup job for a Resource Manager-enabled VM starts, but the VM no longer exists

##**Recommended documents**

 [Azure virtual machine backup monitoring guide](https://azure.microsoft.com/documentation/articles/backup-azure-monitor-vms/)<br>
