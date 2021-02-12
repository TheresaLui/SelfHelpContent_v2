<properties
    pageTitle="SalFileIOError"
    description="We have identified that your backup operation failed during the read operation of the file"
    infoBubbleText="We have identified that your backup operation failed during the read operation of the file: SalFileIOError;"
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-salfileioerror"
    diagnosticScenario="azurebackup-crc-salfileioerror"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>

# Error SalFileIOError

<!--issueDescription-->
We have identified that your backup operation failed during the read operation of the file.
<!--/issueDescription-->

## **Recommended Steps**

 To resolve this issue, perform the below steps:
 
 * Review the properties of the file that is causing the failure and check if it is in the supported [list](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent#supported-file-types-for-backup)
 * Exclude the failed file(s) and retry the backup operation
