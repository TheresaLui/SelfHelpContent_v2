<properties
    pageTitle="My storage service is slow"
    description="My storage service is slow"
    service="microsoft.classicstorage"
    resource="storageaccounts"
    authors="kasparks,passaree"
    ms.author="kasparks,passap"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15629"
    cloudEnvironments="MoonCake"
	articleId="0c7b6a64-35e7-467e-9ee7-cfdc6ecc3614"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My storage service is slow

## **Recommended Steps**

Diagnosing and troubleshooting issues in a distributed application hosted in a cloud environment can be complex. Having [baseline metrics](https://docs.azure.cn/zh-cn/monitoring-and-diagnostics/) available will help you identify where a performance issue may lie. Here are some common scenarios your metrics may turn up, and how to troubleshoot them. 

1. [Metrics show high AverageE2ELatency and low AverageServerLatency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-high-AverageE2ELatency-and-low-AverageServerLatency)
2. [Metrics show low AverageE2ELatency and low AverageServerLatency but the client is experiencing high latency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-low-AverageE2ELatency-and-low-AverageServerLatency)
3. [Metrics show high AverageServerLatency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-high-AverageServerLatency)
4. [You are experiencing unexpected delays in message delivery on a queue](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#you-are-experiencing-unexpected-delays-in-message-delivery)
5. [Metrics show an increase in PercentThrottlingError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError)
6. [Metrics show an increase in PercentTimeoutError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError)
7. [Metrics show an increase in PercentNetworkError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentNetworkError)
8. The client is receiving [HTTP 403](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-403-messages), [HTTP 404](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-404-messages), or [HTTP 409](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-409-messages) error.

For an in-depth look at troubleshooting performance issues, see the Performance section of the article [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)

## **Recommended Documents**

* [How to troubleshoot Storage performance issues](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)
