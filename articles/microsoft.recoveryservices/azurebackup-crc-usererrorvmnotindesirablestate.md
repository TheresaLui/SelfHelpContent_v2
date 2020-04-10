<properties
	pageTitle="UserErrorVmNotInDesirableState"
	description="UserErrorVmNotInDesirableState"
	infoBubbleText="VM is not in a state that allows backups."
	service="microsoft.recoveryservices"
	resource="backup"
	authors="srinathvasireddy"
	ms.author="srinathv"
	displayOrder=""
	articleId="azurebackup-crc-usererrorvmnotindesirablestate"
	diagnosticScenario="azurebackup-crc-usererrorvmnotindesirablestate"
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15207"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorVmVaultLocationMismatch

<!--issueDescription-->
We identified that your backup operation has failed because the VM is in a Failed state. For a successful backup, the VM state should be Running, Stopped, or Stopped (deallocated).
<!--/issueDescription-->

## **Recommended Document**

* [Azure Backup Troubleshooting](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorvmnotindesirablestate---vm-is-not-in-a-state-that-allows-backups)
