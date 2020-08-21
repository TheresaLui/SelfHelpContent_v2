<properties
    pageTitle="CBPStorageClientError"
    description="CBPStorageClientError"
    infoBubbleText="The operation failed because Microsoft Azure Recovery Services Agent was unable to contact Microsoft Azure Backup"
    resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-cbpstorageclienterror"
        diagnosticScenario="azurebackup-crc-cbpstorageclienterror"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

# Error CBPStorageClientError

<!--issueDescription-->
We have identified that your backup operation failed due to an intermittent network issue.  
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, perform the following:

 - Check your [network connectivity](https://docs.microsoft.com/azure/backup/install-mars-agent#verify-internet-access ) and [proxy](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#verifying-proxy-settings-for-windows) settings
 - Transient (intermittent) network bandwidth or network issues might interfer with transfer of backup data to Azure endpoint can result in this failure. Subsequent operations (i.e next scheduled backup or retry) might resolve the issue.

## **Recommended Documents**

 - [Basic troubleshooting](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot#basic-troubleshooting)
 - [Files and folders backup is slow](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue) 
