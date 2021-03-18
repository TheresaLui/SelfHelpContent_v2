<properties
    pageTitle="UserErrorVmNotFoundV2"
    description="UserErrorVmNotFoundV2"
    infoBubbleText="We have identified that your backup operation has failed because the virtual machine does not exist."
    service="microsoft.recoveryservices"
    resource="backup"
    authors="srinathvasireddy"
    ms.author="srinathvasireddy"
    displayOrder=""
    articleId="azurebackup-crc-usererrorvmnotfoundv2"
    diagnosticScenario="azurebackup-crc-usererrorvmnotfoundv2"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15207"
    cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_Backup"
/>


# Error UserErrorVmNotFoundV2

<!--issueDescription-->
If an Azure VM that is configured for Azure Backup is either deleted or moved without [stopping protection]( https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#stop-protecting-a-vm), then the scheduled/on-demand backup job will fail with the error **UserErrorVmNotFoundV2**.
<!--/issueDescription-->

## **Recommended Steps**

- Ensure the Virtual Machine exists or select a different Virtual Machine
- The backup pre-check will appear as critical only for the failed on-demand backup jobs (failed scheduled jobs aren't displayed)
- [Learn more]( https://docs.microsoft.com/azure/backup/backup-azure-manage-vms#backup-item-where-primary-data-source-no-longer-exists)
