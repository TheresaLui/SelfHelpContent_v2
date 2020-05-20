<properties
pageTitle="Connections to storage account were rejected due to lower TLS version"
description="Connections to storage account were rejected due to lower TLS version"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="annayak"
ms.author="annayak"
displayOrder=""
articleId="storagev2insights_acc_connectivity_http_400_TlsVersionNotPermitted"
diagnosticScenario="Connections to storage account were rejected due to lower TLS version"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# Connectivity issues with Storage Firewalls enabled
<!--issueDescription-->
We have detected that minimum TLS Version 1.2 is configured on the storage account and that led to connection rejections from clients using a lower TLS version.
<!--/issueDescription-->

Between **<!--$StartTime-->[StartTime]<!--/$StartTime-->** UTC and **<!--$EndTime-->[EndTime]<!--/$EndTime-->** UTC some connections to the storage account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->** were rejected. The **TLS version** used for these connections is lower than currently permitted on the storage account. At current time, only connections using **[Minimum TLS Version 1.2](https://docs.microsoft.com/azure/storage/common/storage-security-tls)** or higher are allowed to access the storage account, so any client trying to connect with a lower version of TLS will be rejected. You can validate the minimum TLS version setting on the Azure Portal.</br>

**List of sample connections that were rejected:**

<!--$FailedRequestsTable-->[FailedRequestsTable]<!--/$FailedRequestsTable-->

There may be more connections which were rejected. To get the exhaustive list, review the [storage analytics log](https://docs.microsoft.com/azure/storage/common/storage-analytics#about-storage-analytics-logging).

## **Recommended Steps**

1. For the client to negotiate TLS 1.2, the OS and the Application Framework used by the application need to support TLS 1.2. Please refer below to make the necessary changes:

   * [Enable secure TLS for Azure Storage client](https://docs.microsoft.com/azure/storage/common/storage-security-tls)
   * [Enable TLS 1.2 in .NET client](https://docs.microsoft.com/azure/storage/common/storage-security-tls#enable-tls-12-in-net-client)
   * [Enable TLS 1.2 in PowerShell client](https://docs.microsoft.com/azure/storage/common/storage-security-tls#enable-tls-12-in-powershell-client)

2. Validate the OS and Framework support TLS 1.2

   * [Operating system requirements to support TLS 1.2](https://docs.microsoft.com/dotnet/framework/network-programming/tls#support-for-tls-12)
   * [Requirements to support TLS 1.2 with .NET Framework 3.5](https://docs.microsoft.com/dotnet/framework/network-programming/tls#support-for-tls-12)

3. Azure Cloud Service [Web / Worker roles] requirement
   * [Considerations for Web/Worker Roles](https://docs.microsoft.com/dotnet/framework/network-programming/tls#azure-cloud-services)

4. Troubleshoot to find the TLS version used by the application
   * [Use Fiddler to find TLS version](https://docs.microsoft.com/azure/storage/common/storage-security-tls#verify-tls-12-connection)






