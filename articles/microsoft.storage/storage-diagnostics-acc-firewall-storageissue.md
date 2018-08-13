<properties
pageTitle="Storage issues when Storage Firewalls is enabled"
description="Firewall is not compatible with certain Storage operations"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_acc_firewall_disable"
diagnosticScenario="Storage issues when Storage Firewalls is enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Storage issues when Storage Firewalls is enabled

<!--issueDescription-->
We have detected that [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security) is configured on the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Disk Import/Export do not work when Storage Firewalls and Virtual Networks is configured. Storage team is working to fix this issue. In the meantime, please [disable Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security#change-the-default-network-access-rule) and retry the failed operation.
<!--/issueDescription-->

We are sorry to inform you that currently Azure Disk Import/Export do not work when [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security) is configured. Storage team is working to fix this issue. In the meantime, please [disable Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security#change-the-default-network-access-rule) on the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** and retry the failed operation. We sincerely apologize for the inconvienence.