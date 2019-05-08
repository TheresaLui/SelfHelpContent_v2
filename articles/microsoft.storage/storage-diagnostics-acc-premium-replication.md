<properties
pageTitle="Premium storage account only supports LRS replication type"
description="Only LRS replication type is supported"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_acct_type_premium_replication"
diagnosticScenario="Premium storage account only supports LRS replication type"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Premium storage account only supports LRS replication type

<!--issueDescription-->

Storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**  is configured to use premium performance tier which [only supports LRS (Locally redundant storage) replication type](https://docs.microsoft.com/azure/virtual-machines/windows/premium-storage#features). Azure Premium Storage accounts do not support ZRS, GRS, or RA-GRS replication type at this time.

To protect data in premium storage accounts follow our recommended [best practices for backup and disaster recovery of IaaS disks.](https://docs.microsoft.com/azure/virtual-machines/windows/backup-and-disaster-recovery-for-azure-iaas-disks)
<!--/issueDescription-->
