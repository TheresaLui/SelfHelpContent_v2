<properties
	pageTitle="Azure Backup - Backup is taking longer than expected"
	description="Azure Backup - Backup is taking longer than expected"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="13"
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags="windows"
	productPesIds=""
	cloudEnvironments="MoonCake"
	articleId="azurebackup-crp-backupperf-mooncake"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure Backup - Backup is taking longer than expected

## **Recommended Steps**

- Note that a first backup time **can be greater than 24 hours**, as it is proportional to the size of the source data
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete
- Understand the [factors contributing to backup time](https://docs.azure.cn/backup/backup-azure-vms-introduction#backup-performance)
- Follow [best practices](https://docs.azure.cn/backup/backup-azure-vms-introduction#best-practices) to optimize backup performance
