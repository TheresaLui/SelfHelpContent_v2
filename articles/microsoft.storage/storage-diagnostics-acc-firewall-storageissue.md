<properties
pageTitle="Storage issues when Storage Firewalls is enabled"
description="Firewall is not compatible with certain Storage operations"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
ms.author="passap"
displayOrder=""
articleId="Storagev2insights_acc_firewall_disable"
diagnosticScenario="Storage issues when Storage Firewalls is enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Storage issues when Storage Firewalls is enabled

<!--issueDescription-->
We have detected that Storage Firewalls and Virtual Networks is configured on the Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Some Storage services such as blob to blob copy and Disk Import/Export do not work when Storage Firewalls and Virtual Networks is configured. Storage team is working to fix this issue. 
<!--/issueDescription-->

In the meantime, please [disable Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security#change-the-default-network-access-rule) and retry the failed operation.

## **Recommended Documents**
* [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
