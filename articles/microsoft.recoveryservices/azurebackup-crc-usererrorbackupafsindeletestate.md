<properties
      pageTitle="UserErrorBackupAFSInDeleteState"
      description="UserErrorBackupAFSInDeleteState"
      infoBubbleText="The Azure Backup service could not communicate with the VM Agent for triggering snapshot"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-usererrorbackupafsindeletestate"
      diagnosticScenario="azurebackup-crc-usererrorbackupafsindeletestate"
      selfHelpType="diagnostics"
      supportTopicIds="32553277"
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorBackupAFSInDeleteState

<!--issueDescription-->
The file shares blade is displaying the item state by recovering data based on the friendly name, causing a view corresponding to the deleted file share and not to the newly created file share that has the same friendly name. This inconsistency is not present in the vault blade. This issue will be resolved in the upcoming releases.
<!--/issueDescription-->

To resolve this issue, follow the steps listed in [backup failed as the Azure file share is permanently deleted](https://docs.microsoft.com/azure/backup/troubleshoot-azure-files#usererrorbackupafsindeletestate--backup-failed-as-the-associated-azure-file-share-is-permanently-deleted)
