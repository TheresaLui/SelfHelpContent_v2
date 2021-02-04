<properties
      pageTitle="SendCmdToPluginHostFailed"
      description="SendCmdToPluginHostFailed"
      infoBubbleText="This error occurs when the Backup plugin service was not able to start on this machine"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-sendcmdtopluginhostfailed"
      diagnosticScenario="azurebackup-crc-sendcmdtopluginhostfailed"
      selfHelpType="diagnostics"
      supportTopicIds=""
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# SendCmdToPluginHostFailed

<!--issueDescription-->
This error occurs when the Backup plugin service was not able to start on this machine.
<!--/issueDescription-->

To resolve this issue:
1. Navigate to services.msc and ensure that Azure Backup Workload Plugin Service is up and running, with the logon user as *NT Service\AzureWLBackupPluginSvc*
2. Verify that the VM has all the [required permissions](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions). 
