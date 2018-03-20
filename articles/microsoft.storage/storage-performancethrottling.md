<properties
	pageTitle="Troubleshooting Throttling or Performance Errors"
	description="Troubleshooting Throttling or Performance Errors"
	service="microsoft.storage"
	resource="storageaccounts"
	authors="passaree"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32602727"
	resourceTags=""
	productPesIds="16459"
	cloudEnvironments="public"
/>

# My storage service is slow

## **Recommended steps**
Diagnosing and troubleshooting issues in a distributed application hosted in a cloud environment can be complex. Here are some common scenarios your metrics may turn up, and how to troubleshoot them. 

Do you have baseline metrics? The performance of an application can be subjective, especially from a user perspective. Therefore, it is important to have baseline metrics available to help you identify where there might be a performance issue. 

1. [Metrics show an increase in PercentThrottlingError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentThrottlingError)
2. [Metrics show an increase in PercentTimeoutError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentTimeoutError)
3. [Metrics show an increase in PercentNetworkError](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#metrics-show-an-increase-in-PercentNetworkError)
4. The client is receiving [HTTP 403](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-403-messages), [HTTP 404](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-404-messages), or [HTTP 409](https://azure.microsoft.com/documentation/articles/storage-monitoring-diagnosing-troubleshooting/#the-client-is-receiving-409-messages) error.

For an in-depth look at troubleshooting performance issues, see the Performance section of the article [**Monitor, diagnose, and troubleshoot Microsoft Azure Storage**](http://go.microsoft.com/fwlink/?LinkId=785091)

## **Recommended documents**
[How to troubleshoot Storage performance issue?](http://go.microsoft.com/fwlink/?LinkId=785091)<br>
[What are the Storage account scalability limits?](http://go.microsoft.com/fwlink/?LinkId=785092)