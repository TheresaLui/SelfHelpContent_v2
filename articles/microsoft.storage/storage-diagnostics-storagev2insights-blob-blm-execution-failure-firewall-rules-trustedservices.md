<properties
pageTitle="Lifecycle Management doesnot execute when Firewall is enabled without Trusted Services selected"
description="Lifecycle Management doesnot execute when Firewall is enabled without Trusted Services selected"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_blob_blm_execution_firewall_rules_trustedservices"
diagnosticScenario="Storage issues with Storage Firewalls enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Lifecycle Management doesn't execute when Storage Firewall is enabled without "Trusted Services" selected

<!--issueDescription-->
We have detected that Storage Firewalls and Virtual Networks is currently configured on the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**, but doesn't have **Trusted Microsoft** services selected as an exception. Lifecycle management requests are issued via the Microsoft.Insights service which is a trusted Microsoft Service. These requests get blocked when **Trusted Microsoft Services** is not selected in the firewall exception list.
<!--/issueDescription-->

## **Recommended Steps**

* For successful execution of Lifecycle management policies on the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** , add **Trusted Services** as an exception

## **Recommended Documents**

 * [Configure firewall and virtual networks Exception](https://docs.microsoft.com/azure/storage/common/storage-network-security#exceptions)
 * [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security)
 * [Trusted Microsoft Services](https://docs.microsoft.com/azure/storage/common/storage-network-security#trusted-microsoft-services)
