<properties
	pageTitle="Azure virtual machine backups are running slow"
	description="VM backup performance"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="20"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-iaas-backupperf-mooncake"
	ownershipId="Compute_SiteRecovery"
/>

# Azure virtual machine backups are running slow

## **Recommended Steps**

- First backup time **can be greater than 24 hours**, as it is proportional to size of source data
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete
- Understand the [factors contributing to backup time.](https://docs.azure.cn/backup/backup-azure-vms-introduction#backup-performance)
- Follow [best practices](https://docs.azure.cn/backup/backup-azure-vms-introduction#best-practices) to optimize backup performance
