<properties
	pageTitle="Azure Files & Folders Backup"
	description="Files & Folders Backup Install Registration issues"
	service="microsoft.recoveryservices"
	resource="vaults"
	authors="pvrk"
	ms.author="pvrk"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32553287"
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1172727d-c1b2-42cb-8ecc-0ad36a9d1574"
	ownershipId="StorageMediaEdge_Backup"
/>

# Install and Registration failures for Files and Folders backup

## **Recommended Steps**

To resolve common install and registration issues, choose the symptom you are observing:

- [Invalid vault credentials provided](https://aka.ms/invalidvaultcredentials)
- Microsoft Azure subscription has expired

If the subscription has not expired but you are still facing this error, run the following command in Azure Powershell in the context of the concerned subscription: `Register-AzureRmResourceProvider-ProviderNamespace Microsoft.RecoveryServices`
	
Wait for 30mins to check the status using the command `Get-AzureRmResourceProvider-ProviderNamespace Microsoft.RecoveryServices`
	
- [Failed to set the encryption key for secure backups](https://aka.ms/MABAgentEncryptionKeyError)
- [The Microsoft Azure Recovery Service Agent was unable to connect to Microsoft Azure Backup](https://aka.ms/MABagentUnableToConnect)
- [The activation did not complete successfully. The current operation failed due to an internal service error.](https://aka.ms/MABAgentActivationError)


## **Recommended Documents**

- [Step by step guide to setup files and folder backup using Azure Backup Agent](https://aka.ms/AB-AA4dwtm)
- [Network and Connectivity Requirements for Files and Folders Backup](https://aka.ms/AB-MARS-networkconnectivity)
- [Pricing details](https://azure.microsoft.com/pricing/details/backup/)
- [Frequently asked questions](https://aka.ms/AB-MARS-FAQ)
