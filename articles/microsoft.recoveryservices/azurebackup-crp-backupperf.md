<properties
	pageTitle="Azure Backup - Backup is taking longer than expected"
	description="Azure Backup - Backup is taking longer than expected"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="9"
	selfHelpType="resource"
	supportTopicIds="32637321"
	resourceTags="windows"
	productPesIds="15571,15797,16470,16454,14749"
	cloudEnvironments="public"
	articleId="fdee12e71-369d-4812-9400-8a81bd302190"
/>

# Azure Backup - Backup is taking longer than expected

## **Recommended Steps**

- Note that a first backup time **can be greater than 24 hours**, as it is proportional to the size of the source data
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete
- Understand the [factors contributing to backup time](https://aka.ms/AB-AA4ecqb) <br>
- Follow [best practices](https://aka.ms/AB-AA4e56d) to optimize backup performance
