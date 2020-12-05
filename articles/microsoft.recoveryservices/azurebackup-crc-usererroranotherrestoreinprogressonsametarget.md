<properties
      pageTitle="UserErrorAnotherRestoreInProgressOnSameTarget"
      description="UserErrorAnotherRestoreInProgressOnSameTarget"
      infoBubbleText="The Azure Backup service could not communicate with the VM Agent for triggering snapshot"
      service="microsoft.recoveryservices"
      resource="backup"
      authors="srinathv"
      ms.author="srinathv"
      articleId="azurebackup-crc-usererroranotherrestoreinprogressonsametarget"
      diagnosticScenario="azurebackup-crc-usererroranotherrestoreinprogressonsametarget"
      selfHelpType="diagnostics"
      supportTopicIds=""
      productPesIds="15207"
      cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# UserErrorAnotherRestoreInProgressOnSameTarget

<!--issueDescription-->
Your restore operation might have failed because another restore job is in progress on the same target file share.
<!--/issueDescription-->

To resolve this issue, use a different target file share. Alternatively, you can cancel or wait for the other restore to complete.
