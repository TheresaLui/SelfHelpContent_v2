<properties
        pageTitle="BMSUserErrorObjectLocked"
        description="BMSUserErrorObjectLocked"
        infoBubbleText="Another operation is in progress on the selected item"
        resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-bmsusererrorobjectlocked"
        diagnosticScenario="azurebackup-crc-bmsusererrorobjectlocked"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

# Error BMSUserErrorObjectLocked
 
<!--issueDescription-->

We have identified that your operation for enabling the backup failed because another operation is in progress.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the following:
- Ensure the operation currently in progress is completed and retry the backup. For more info, refer to this [article](https://docs.microsoft.com/azure/backup/troubleshoot-azure-files#bmsusererrorobjectlocked--another-operation-is-in-progress-on-the-selected-item)
- Review the backup scheduling limits listed in this [article](https://docs.microsoft.com/azure/backup/backup-azure-backup-faq#are-there-limits-on-backup-scheduling)
