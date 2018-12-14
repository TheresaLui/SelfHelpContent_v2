<properties
    pageTitle="Azure Stack infrastructure backup"
    description=""
    service="microsoft.azurestack"
    resource="azurestack"
    authors="alexsmithMSFT"
    authorAlias="alexsmit"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32629173,32629196,32629217,32629218,32629219,32629252"
    resourceTags=""
    productPesIds="16226"
    cloudEnvironments="public"
/>

# Azure Stack infrastructure backup

## **Recommended steps**

You can backup and restore configuration and service data using the Infrastructure Backup Service. Backups created by the service can be used for the redeployment of the Azure Stack Cloud to to restore identity, security, and Azure Resource Manager data.

1. Make sure you have [met all prerequisites](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-infrastructure-backup#verify-requirements-for-the-infrastructure-backup-service) for Azure Stack infrastructure backup
2. [Enable backup for Azure Stack from the administration portal](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-enable-backup-console)
3. [Back up Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-back-up-azure-stack) infrastructure components
4. [Confirm backup has completed successfully](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-back-up-azure-stack#confirm-backup-has-completed)
5. If necessary, [recover from catastrophic data loss](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-recover-data)

## **Recommended documents**

[Infrastructure Backup Service best practices](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-best-practices)<br>
[Enable Backup for Azure Stack from the administration portal](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-enable-backup-console)<br>
[Back up Azure Stack](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-back-up-azure-stack)<br>
[Recover from catastrophic data loss](https://docs.microsoft.com/azure/azure-stack/azure-stack-backup-recover-data)<br>