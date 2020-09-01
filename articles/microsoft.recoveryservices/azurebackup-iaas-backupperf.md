<properties
	pageTitle="Azure virtual machine backups are running slow"
	description="VM backup performance"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="3"
	selfHelpType="generic"
	supportTopicIds="32553281"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="870b74fd-a900-42a7-bdd1-a706fa8b2558"
	ownershipId="StorageMediaEdge_Backup"
/>

# Azure virtual machine backups are running slow

## **Recommended steps**
- First backup time **can be greater than 24 hours**, it is proportional to size of source data. <br>
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete. <br>
- Understand the [factors contributing to backup time.](https://aka.ms/AB-AA4ecqb) <br>
- Follow [best practices](https://aka.ms/AB-AA4e56d) to optimize backup performance. <br>
