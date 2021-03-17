<properties
        pageTitle="ExtensionInstallationFailure"
        description="ExtensionInstallationFailure"
        infoBubbleText="Backup extension installation failed"
        resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-extensioninstallationfailure"
        diagnosticScenario="azurebackup-crc-extensioninstallationfailure"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

# Extension Installation Failure

<!--issueDescription-->

We have identified that your operation for enabling the backup failed because Azure Backup service failed to install backup extension on the Azure VM.
<!--/issueDescription-->

## **Recommended Steps**

1. Extension installation could fail because of the internal error **ExtensionVCRedistInstallationFailure**. To resolve this issue, follow [these steps](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionvcredistinstallationfailure---the-snapshot-operation-failed-because-of-failure-to-install-visual-c-redistributable-for-visual-studio-2012).

2. If you have an antivirus product in place, ensure that it includes the correct exclusion rules to allow the installation.

3. If SQL Server is running on Azure VM, follow these steps: 
 * Ensure that SQL Server meets the support requirements and prerequisites listed in this [article](https://docs.microsoft.com/azure/backup/sql-support-matrix)
 * Check if the user account has SQL Server system admin permissions. Follow [these steps](https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) to provide system admin permissions on the VM.
