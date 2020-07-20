<properties
  pageTitle="We ran an analysis of your Cache"
  description="Diagnostic Template"
  infoBubbleText="We ran performance analysis on your cache. See details on the right."
  service="microsoft.cache"
  resource="redis"
  authors="igamigo"
  ms.author="igamigo"
  displayOrder=""
  articleId="cache-diagnostics-analysisinsight"
  diagnosticScenario=""
  selfHelpType="diagnostics"
  supportTopicIds=""
  resourceTags=""
  productPesIds="14783"
  cloudEnvironments="public"
  ownershipId="RedisCache_RedisCache"
/>

# We ran diagnostics on your resource and found potential client-side performance problems

<!--issueDescription-->
We ran diagnostics on your Cache **<!--$ResourceName-->ResourceName<!--/$ResourceName-->** from **<!--$StartTime-->StartTime<!--/$StartTime-->** through to <!--$EndTime-->EndTime<!--/$EndTime--> and found some potential issues related to the client usage.

<!--/issueDescription-->

The following aspects of the instance's metrics should be reviewed:

<!--$Recommendation-->Recommendation<!--/$Recommendation-->


## **Recommended Steps**

1. Implement our [best practices](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-best-practices) to make sure the client application is making good use of the cache
1. Review the client application health to check for related symptoms
1. Review the documentation article related to [client-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client)


## **Recommended Documents**

* [Troubleshoot Azure Cache for Redis client-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client)
* [Failover and patching - Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-failover)

