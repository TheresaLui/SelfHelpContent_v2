<properties
	pageTitle="pitmanagerdataplaneiofail.md"
	description="pitmanagerdataplaneiofail.md"
	infoBubbleText="network connectivity issues"
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathvasireddy"
	displayOrder=""
	articleId="azurebackup-crc-pitmanagerdataplaneiofail"
	diagnosticScenario="azurebackup-crc-pitmanagerdataplaneiofail"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error PitManagerDataPlaneIoFail

<!--issueDescription-->
We have identified that your backup operation failed due to network connectivity issues.  
<!--/issueDescription-->

## **Recommended Document**

- Ensure there is [network connectivity to Azure backup service](https://docs.microsoft.com/azure/backup/backup-sql-server-database-azure-vms#establish-network-connectivity)
- Additionally, if private endpoint is enabled on the vault, change the host file to resolve the backup/storage account FQDN to the private IP address or setup private DNS zone. [Learn more](https://docs.microsoft.com/azure/backup/private-endpoints#create-dns-zones-for-custom-dns-servers)
- If private DNS zone is not feasible, then set up DNS configuration for private endpoint using the host file. [Learn more](https://docs.microsoft.com/azure/private-link/private-endpoint-dns)
