<properties
	pageTitle="Backup failures while using Azure Backup agent"
	description="Common issues during backup of files and folders using Azure Backup agent"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="pvrk"
	ms.author="pvrk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553275"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, MoonCake, fairfax, usnat, ussec"
	articleId="fc3023bd-b8cf-4451-a14d-76e1a8ba8c15"
	ownershipId="StorageMediaEdge_Backup"
/>

# Backup of files and folders with Azure Backup Agent fails

## **Recommended Steps**

- [Ensure Microsoft Azure Recovery Services (MARS) Agent is up to date before troubleshooting further](https://go.microsoft.com/fwlink/?linkid=229525&clcid=0x409) <br>
- [Ensure there is network connectivity between MARS agent and Azure](https://aka.ms/AB-A4dp50) <br>
- Ensure Microsoft Azure Recovery Services is running (in Service console). If required restart and retry the operation <br>
- [Ensure 5-10% free volume space is available on scratch folder location](https://aka.ms/AB-AA4dwtt) <br>
- [Check if another process or antivirus software is interfering with Azure Backup](https://aka.ms/AB-AA4dwtk) 
- [Scheduled backup fails, but manual backup works](https://aka.ms/ScheduledBackupFailManualWorks) <br>
- Ensure your OS has the latest updates <br>
- [Troubleshooting common Azure Backup agent issues](https://aka.ms/AB-AA4dp4y)

## **Recommended Documents**

- [Invalid vault credentials provided](https://aka.ms/AB-AA4dwts)<br>
- [Failed to download the vault credential file](https://aka.ms/AAB-unable-to-download-vault-credential-file)<br>
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://aka.ms/AB-AA4dy33)<br>
- [(407) Proxy Authentication Required](https://aka.ms/AB-AA4dy33)<br>
- [Failed to set the encryption key for secure backup](https://aka.ms/AB-AA4dp56)<br>
- [Activation did not succeed completely but the encryption passphrase was saved to the following file](https://aka.ms/AB-AA4dp56)<br>
- [Encryption passphrase not correctly configured](https://aka.ms/AB-AA4dwto)
