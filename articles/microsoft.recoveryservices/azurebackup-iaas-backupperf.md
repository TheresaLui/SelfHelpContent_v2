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
- First backup time **can be greater than 24 hours**, it is proportional to size of source data. <br> 
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete. <br> 
- Understand the [factors contributing to backup time.](https://azure.microsoft.com/documentation/articles/backup-azure-vms-introduction/#total-vm-backup-time) <br> 
- Follow [best practices](https://azure.microsoft.com/documentation/articles/backup-azure-vms-introduction/#best-practices) to optimize backup performance. <br>
