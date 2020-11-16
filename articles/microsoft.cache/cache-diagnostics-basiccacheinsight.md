<properties
  pageTitle="Your cache belongs to the Basic SKU"
  description="Diagnostic Template"
  infoBubbleText="Basic caches have limitations."
  service="microsoft.cache"
  resource="redis"
  authors="igamigo"
  ms.author="igamigo"
  displayOrder=""
  articleId="cache-diagnostics-basiccacheinsight"
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
Your Cache **<!--$ResourceName-->ResourceName<!--/$ResourceName-->** is a cache from the **Basic** tier, a simplified service that is ideal for development and testing.

These caches do not have high availability and are expected to incur in data loss or brief unavailability whenever a maintenance operation is performed on the underlying resources, such as reboots or patching. There is no Service Level Agreement on the Basic tier. If you are using this cache for production, we highly recommend upgrading to a Standard or Premium tier.
<!--/issueDescription-->

## **Recommended Documents**

* [Azure Cache for Redis - Service Tiers](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-overview#service-tiers)
* [Azure Cache for Redis pricing](https://azure.microsoft.com/pricing/details/cache/)
* [Failover and patching - Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-failover)
