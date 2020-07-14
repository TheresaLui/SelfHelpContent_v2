<properties
	pageTitle="Offline backup or seeding issues"
	description="Offline backup or seeding issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32632796"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="05681e38-121a-41ac-8f38-076a63a92649"
	ownershipId="StorageMediaEdge_Backup"
/>

# Offline backup or seeding issues

## **Recommended Documents**

- [Supported configurations](https://aka.ms/AB-offlineSeeding-Supportedconfig) and [Prerequisites](https://aka.ms/AB-AA4dp4z) for offline backup using Microsoft Azure Recovery Services agent<br>
- [Configure offline backup using Microsoft Azure Recovery Services agent](https://aka.ms/AB-OfflineSeeding-configuration)

**Note:**

- If the source computer is a virtual machine, then the copy computer must be a different physical server or client machine from the source computer<br>
- Ensure that the carrier information and tracking number are updated within two weeks of Azure import job creation. Failure to verify this information within two weeks can result in the job being deleted, and drives not being processed<br>
- Ensure that Azure PowerShell version 3.7.0 is installed on both source and copy computer before you begin offline backup operation
