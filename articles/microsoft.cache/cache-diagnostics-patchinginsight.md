<properties
  pageTitle="We patched your Cache"
  description="Diagnostic Template"
  infoBubbleText="We patched your Cache. See details on the right."
  service="microsoft.cache"
  resource="redis"
  authors="asasine"
  ms.author="adsasine"
  displayOrder=""
  articleId="cache-diagnostics-patchinginsight"
  diagnosticScenario=""
  selfHelpType="diagnostics"
  supportTopicIds=""
  resourceTags=""
  productPesIds="14783"
  cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="RedisCache_RedisCache"
/>

# We ran diagnostics on your resource and found we patched your Cache

<!--issueDescription-->
Our internal service patched your Cache **<!--$ResourceName-->ResourceName<!--/$ResourceName-->** at **<!--$StartTime-->StartTime<!--/$StartTime-->**. During the patching process, client applications would experience connection related errors when communicating to your Cache endpoint. When the patching process completes, client applications should be able to reconnect reliably.

The Azure Cache for Redis service regularly performs maintenance to update your cache with the latest platform features and fixes. Client applications should be written in a way to be resilient to short-lived connection breaks. Data loss is unlikely to occur when using Standard or Premium tier but you can guard against data loss by using data export and persistence. By following the recommended steps below, you can safeguard your Cache from further issues related to patching.
<!--/issueDescription-->

## **Recommended Steps**

1. Implement our [best practices](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-best-practices) to create a system resilient to connection breaks
1. Configure your client library to use a connect timeout of at least 15 seconds
1. [Schedule updates](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-administration#schedule-updates) for a maintenance window to reduce impact on your system
1. Test your system's resiliency to connection breaks using a [reboot](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-administration#reboot) to simulate a patch
1. Enable [persistence](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-premium-persistence) or periodically [export](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-import-export-data) your Cache's data to further prevent data loss

## **Recommended Documents**

* [Failover and patching - Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-failover)
