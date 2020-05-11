<properties
pageTitle="High E2E Latency due to client side network issues"
description="High E2E Latency due to client side network issues"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="ramMSFT"
ms.author="raprasad"
displayOrder=""
articleId="Storage_HighE2ELatency_ClientNetworkError"
diagnosticScenario="High E2E Latency due to client side network issues"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>

# High E2E Latency caused due to client side network issues
<!--issueDescription-->
We observed that at **<!--$Timeframe-->[Timeframe]<!--/$Timeframe-->** the operation **<!--$Operation-->[Operation]<!--/$Operation-->** on the **<!--$RequestURL-->[RequestURL]<!--/$RequestURL-->** by the **<!--$UserAgent-->[UserAgent]<!--/$UserAgent-->** caused a Network Error. The Total E2E latency is **<!--$TimeInMS-->[TimeInMS]<!--/$TimeInMS-->**. We observed **<!--$ReadWriteLatency-->[ReadWriteLatency]<!--/$ReadWriteLatency-->** latency and NetworkDisconnect error from our Server Logs for **<!--$Optype-->[Optype]<!--/$Optype-->**, which indicates that Storage was unable to **<!--$ReadFromWriteTo-->[ReadFromWriteTo]<!--/$ReadFromWriteTo-->** the client due to client side network issues causing the error.
<!--/issueDescription-->

## **Recommended Steps**

* Identify and resolve [client side performance issues](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?toc=%2fazure%2fstorage%2fblobs%2ftoc.json#investigating-client-performance-issues) 
* Refer to [troubleshooting network latency issues](https://docs.microsoft.com/azure/storage/common/storage-monitoring-diagnosing-troubleshooting?toc=/azure/storage/blobs/toc.json#investigating-network-latency-issues) to further troubleshoot Network issues
