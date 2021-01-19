<properties
	pageTitle="CBPStorageServerError"
	description="CBPStorageServerError"
	infoBubbleText="The operation failed because Microsoft Azure Recovery Services Agent was unable to contact Microsoft Azure Backup"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathv"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-cbpstorageservererror"
	diagnosticScenario="azurebackup-crc-cbpstorageservererror"
	selfHelpType="diagnostics"
	supportTopicIds=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# CBPStorageServerError

<!--issueDescription-->
The operation failed because Microsoft Azure Recovery Services Agent was unable to contact Microsoft Azure Backup.
<!--/issueDescription-->

## **Recommended Steps**

1. Verify that you are connected to the internet
2. [Proxy server settings are configured correctly](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#verifying-proxy-settings-for-windows)
3. [Check if your firewall, VPN or proxy server is blocking calls to azure endpoints](https://docs.microsoft.com/azure/backup/install-mars-agent#verify-internet-access)
