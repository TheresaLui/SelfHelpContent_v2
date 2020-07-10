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

# Error ExtensionInstallationFailure

<!--issueDescription-->

We have identified that your operation for enabling the backup failed because Azure backup service failed to install backup extension on the Azure VM.
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the following:
1.	Extension installation could fail because of internal error ‘ExtensionVCRedistInstallationFailure’. To solve this error, follow the steps listed in this [article]( https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#extensionvcredistinstallationfailure---the-snapshot-operation-failed-because-of-failure-to-install-visual-c-redistributable-for-visual-studio-2012).
2.	If you have antivirus products in place, ensure they have the right exclusion rules to allow the installation.
3.	If the Azure VM is an SQL server then – 
- Ensure it meets the support requirements and pre-requisites listed in this [article]( https://docs.microsoft.com/azure/backup/sql-support-matrix).
- Check if the user account has SQL Server sysadmin permissions. Follow the steps listed in this [article]( https://docs.microsoft.com/azure/backup/backup-azure-sql-database#set-vm-permissions) to provide Sysadmin rights on the VM. 
