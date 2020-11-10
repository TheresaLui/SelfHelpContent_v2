<properties
	pageTitle="Files and Folder Backup Restore failures"
	description="Files and Folder Backup Restore failures"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553296"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="9d7bb66b-c9c0-47fa-bbcf-636e88c8c090"
	ownershipId="StorageMediaEdge_Backup"
/>

# Restore of files and folders with Azure Backup Agent fails

## **Recommended Steps**

- [Invalid vault credentials provided: The file is either corrupted or does not have the latest information](https://aka.ms/AB-AA4ecqg)<br>
- The vault credentials provided are **different from the vault this server is registered to:** to recover the data to different machine, the Target machine and the Source machine must be registered with the **same Recovery Services vault** and use the **same Vault Credentials key** at the time of restoration<br>
- Known Limitation: The target VM's operating system version must be **greater than or equal to** source VM's operating system version for successful restore<br>
- If you are trying to restore to alternate location/server, **use the same passphrase** that was initially used during backup <br>
- How to restore files to: [**original location**](https://aka.ms/AB-AA4dwtj) (or) [**alternative location**](https://aka.ms/AA4f1qz)<br>
- [Troubleshooting common restore issues](https://aka.ms/AB-AA4dp4y) <br>
