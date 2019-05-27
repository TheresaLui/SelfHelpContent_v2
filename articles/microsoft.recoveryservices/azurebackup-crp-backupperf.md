<properties
	pageTitle="Azure virtual machine backups are running slow"
	description="VM backup performance"
	service="microsoft.compute"
	resource="virtualmachines"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds="32637321"
	resourceTags=""
	productPesIds="14749"
	cloudEnvironments="public"
	articleId="fdee12e71-369d-4812-9400-8a81bd302190"
/>

# Azure virtual machine backups are running slow

## **Recommended steps**
- First backup time **can be greater than 24 hours**, it is proportional to size of source data. <br>
- Subsequent (i.e. incremental or daily) backup time **can take up to 24 hours** to complete. <br>
- Understand the [factors contributing to backup time.](https://aka.ms/AB-AA4ecqb) <br>
- Follow [best practices](https://aka.ms/AB-AA4e56d) to optimize backup performance. <br>
