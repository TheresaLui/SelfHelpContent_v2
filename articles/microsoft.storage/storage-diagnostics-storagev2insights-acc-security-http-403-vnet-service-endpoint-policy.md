<properties
pageTitle="Connections to storage account endpoint were blocked due to VNet Service Endpoint Policy rules"
description="Connections to storage account endpoint were blocked due to VNet Service Endpoint Policy rules"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_security_http_403_vnet_service_endpoint_policy"
diagnosticScenario="health_diagnostic"
selfHelpType="diagnostics"
supportTopicIds=""
resourceTags="windows"
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connections to storage account endpoint were blocked due to VNet Service Endpoint Policy rules 
<!--issueDescription-->
Some requests to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were blocked between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** and **<!--$EndTime-->[EndTime]<!--/$EndTime-->**. The current **VNET service endpoint policy** on the subnet, where the traffic originated doesn't allow connecting to this storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**.
<!--/issueDescription-->

Only the following subnets have **VNet endpoint policy** that allows access to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**.

**<!--$Subnet_List-->[Subnet_List]<!--/$Subnet_List-->**

Sample list of requests were blocked:
**<!--$IP_RequestUrl-->[IP_RequestUrl]<!--/$IP_RequestUrl-->**

There may be additional client IPs for which requests were blocked. To view the complete list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Documents**

Services running inside a VNet with service endpoint policy must add the storage account **{ResourceName}** explicitly in the policy.
Refer below to make the necessary changes:

1. [Virtual network service endpoint policies](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview)
2. [Configure VNet endpoint policies for Azure Storage](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#configuration)
3. [Limitations](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#limitations)
4. [Logging and troubleshooting](https://docs.microsoft.com/azure/virtual-network/virtual-network-service-endpoint-policies-overview#logging-and-troubleshooting)
