<properties
	pageTitle="My storage service is slow"
	description="My storage service is slow"
	service="microsoft.classicstorage"
	resource="storageaccounts"
	authors="kasparks,passaree"
	displayOrder="5"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="349d34f0-e6b3-4132-aeee-5261602387dd"
	ownershipId="StorageMediaEdge_AccountManagement"
/>

# My storage service is slow

## **Recommended steps**
Diagnosing and troubleshooting issues in a distributed application hosted in a cloud environment can be complex. Here are some common scenarios your metrics may turn up, and how to troubleshoot them. 

Do you have baseline metrics? The performance of an application can be subjective, especially from a user perspective. Therefore, it is important to have baseline metrics available to help you identify where there might be a performance issue. 

1. [Metrics show high AverageE2ELatency and low AverageServerLatency](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-high-AverageE2ELatency-and-low-AverageServerLatency)
2. [Metrics show low AverageE2ELatency and low AverageServerLatency but the client is experiencing high latency](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-low-AverageE2ELatency-and-low-AverageServerLatency)
3. [Metrics show high AverageServerLatency](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-high-AverageServerLatency)
4. [You are experiencing unexpected delays in message delivery on a queue](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#you-are-experiencing-unexpected-delays-in-message-delivery)
5. [Metrics show an increase in PercentThrottlingError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentThrottlingError)
6. [Metrics show an increase in PercentTimeoutError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentTimeoutError)
7. [Metrics show an increase in PercentNetworkError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentNetworkError)
8. The client is receiving [HTTP 403](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-403-messages), [HTTP 404](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-404-messages), or [HTTP 409](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-409-messages) error.

For an in-depth look at troubleshooting performance issues, see the Performance section of the article [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](http://go.microsoft.com/fwlink/?LinkId=785091)

## **Recommended documents**
[How to troubleshoot Storage performance issue?](http://go.microsoft.com/fwlink/?LinkId=785091)
