<properties
	pageTitle="Azure virtual machine backups are running slow"
	description="VM backup performance"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="trinadhk"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds="32553281"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Azure virtual machine backups are running slow

## **Recommended steps**
Understand the factors contributing to backup time and how you can optimize the time by following best practices. <br>
* First backup time is proportional to size of source data and **can be greater than 24 hours**, monitor for the operation to complete.
* Subsequent (i.e. incremental or daily) backups could take upto 24 hours, monitor for the operation to complete. If it exceeds 24 hours, then contact Microsoft support. <br> 

## **Recommended documents**
* Understand the [factors contributing to backup time.](https://azure.microsoft.com/documentation/articles/backup-azure-vms-introduction/#total-vm-backup-time)
* Make sure that you are following [best practices](https://azure.microsoft.com/documentation/articles/backup-azure-vms-introduction/#best-practices) for optimal backup performance. 
* [Planning for Azure virtual machine backup](https://azure.microsoft.com/documentation/articles/backup-azure-vms-introduction/)<br>
