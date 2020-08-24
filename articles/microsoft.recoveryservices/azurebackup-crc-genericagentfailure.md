<properties
        pageTitle="GenericAgentFailure"
        description="GenericAgentFailure"
        infoBubbleText="The operation failed because of a protection agent failure. Retry the operation"
        resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-genericagentfailure"
        diagnosticScenario="azurebackup-crc-genericagentfailure"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

 

# Error GenericAgentFailure

 
<!--issueDescription-->

We have identified that your backup operation could not complete due to protection agent failure.
<!--/issueDescription-->



## **Recommended Steps**

To resolve this issue, perform the following:

- Ensure Antivirus is disabled (or) all the correct [exclusions](https://docs.microsoft.com/azure/backup/backup-azure-troubleshoot-slow-backup-performance-issue?branch=pr-112823#cause-another-process-or-antivirus-software-interfering-with-azure-backup) for MARS agent are in place
- Review unsupported files from logs and add them from [exclusion](https://docs.microsoft.com/azure/backup/backup-azure-manage-mars#add-exclusion-rules-to-existing-policy) rules

## **Recommended Documents**

- How to [Troubleshoot the Microsoft Azure Recovery Services (MARS) agent](https://docs.microsoft.com/azure/backup/backup-azure-mars-troubleshoot)
- Review the [supported/unsupported configurations for backup using MARS agent](https://docs.microsoft.com/azure/backup/backup-support-matrix-mars-agent)
