<properties
	pageTitle="Troubleshooting Throttling or Performance Errors"
	description="Troubleshooting Throttling or Performance Errors"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32551679"
	resourceTags=""
	productPesIds="15629"
	cloudEnvironments="MoonCake"
/>

# My storage service is slow

## **Recommended steps**
Diagnosing and troubleshooting issues in a distributed application hosted in a cloud environment can be complex. Here are some common scenarios your metrics may turn up, and how to troubleshoot them. 

Do you have baseline metrics? The performance of an application can be subjective, especially from a user perspective. Therefore, it is important to have baseline metrics available to help you identify where there might be a performance issue. 

1. [Metrics show an increase in PercentThrottlingError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentThrottlingError)
2. [Metrics show an increase in PercentTimeoutError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentTimeoutError)
3. [Metrics show an increase in PercentNetworkError](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#metrics-show-an-increase-in-PercentNetworkError)
4. The client is receiving [HTTP 403](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-403-messages), [HTTP 404](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-404-messages), or [HTTP 409](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting#the-client-is-receiving-409-messages) error.

For an in-depth look at troubleshooting performance issues, see the Performance section of the article [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)

## **Recommended documents**
[How to troubleshoot Storage performance issue?](https://docs.azure.cn/storage/common/storage-monitoring-diagnosing-troubleshooting)<br>
[What are the Storage account scalability limits?](https://docs.azure.cn/storage/common/storage-performance-checklist)
