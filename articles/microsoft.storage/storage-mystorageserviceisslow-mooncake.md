<properties
    pageTitle="My storage service is slow"
    description="My storage service is slow"
    service="microsoft.storage"
    resource="storageaccounts"
    authors="kasparks"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="3dd013ca-c5c9-4e22-bebe-b9ff7257b91e"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My storage service is slow

## **Recommended steps**

Diagnosing and troubleshooting issues in a distributed application hosted in a cloud environment can be complex. Here are some common scenarios your metrics may turn up, and how to troubleshoot them. 

Do you have baseline metrics? The performance of an application can be subjective, especially from a user perspective. Therefore, it is important to have baseline metrics available to help you identify where there might be a performance issue.

1. [Metrics show high AverageE2ELatency and low AverageServerLatency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-high-AverageE2ELatency-and-low-AverageServerLatency)
2. [Metrics show low AverageE2ELatency and low AverageServerLatency but the client is experiencing high latency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-low-AverageE2ELatency-and-low-AverageServerLatency)
3. [Metrics show high AverageServerLatency](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-high-AverageServerLatency)
4. [You are experiencing unexpected delays in message delivery on a queue](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#you-are-experiencing-unexpected-delays-in-message-delivery)
5. [Metrics show an increase in PercentThrottlingError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError)
6. [Metrics show an increase in PercentTimeoutError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError)
7. [Metrics show an increase in PercentNetworkError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentNetworkError)
8. The client is receiving [HTTP 403](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-403-messages), [HTTP 404](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-404-messages), or [HTTP 409](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-409-messages) error.

For an in-depth look at troubleshooting performance issues, see the Performance section of the article [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)

## **Recommended documents**

* [How to troubleshoot Storage performance issue?](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)