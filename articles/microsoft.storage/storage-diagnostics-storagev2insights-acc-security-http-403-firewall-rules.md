<properties
pageTitle="Connections to storage account were blocked due to firewall rules"
description="Connections to storage account were blocked due to firewall rules"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_firewall_rules"
diagnosticScenario="Storage issues with Storage Firewalls enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connectivity issues with Storage Firewalls enabled

We have detected that [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security) is configured on the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**.

<!--issueDescription-->
Between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** UTC and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** UTC certain connections to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked. The current **firewall** rule on the storage account doesn't allow traffic originating from those IP addresses.
<!--/issueDescription-->

Only the following IPs or VNet/subnet are allowed to access storage account:

**<!--$Allowed_IPs-->[Allowed_IPs]<!--/$Allowed_IPs-->**

Sample list of client IPs for which the requests were blocked:

**<!--$IP_RequestUrl-->[IP_RequestUrl]<!--/$IP_RequestUrl-->**

There may be more client IPs for which requests were blocked. To get the exhaustive list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps**

1. Third-party services running outside Azure must ensure that their IPs are in the allowed list when Storage Firewalls and Virtual Networks is configured. Validate that the client IPs are expected to connect to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** and refer below to make the necessary changes:

   * [Change the default network access rule](https://docs.microsoft.com/azure/storage/common/storage-network-security#change-the-default-network-access-rule)
   * [Grant access from an Internet IP range](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range)

2. For services running in Azure, the VNet the service is part of needs to added to the allowed list when Storage Firewalls and Virtual Networks is configured:

   * [Grant access from a Virtual Network](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-a-virtual-network)

3. For clients behind a proxy, the exception should be made for the [public IP](http://www.whatsmyip.org/) of the proxy server.
4. A general recommendation is to enable [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging) to trace requests, analyze usage trends, and diagnose issues with your storage account.


