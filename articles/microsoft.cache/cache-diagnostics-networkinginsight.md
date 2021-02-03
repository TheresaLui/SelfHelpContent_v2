<properties
    pageTitle="Instances of metrics near the capacity limits detected"
    description="Instances of metrics near the capacity limits detected"
    infoBubbleText="Unhealthy metrics found for the cache "
    service="microsoft.cache"
    resource="redis"
    authors="igamigo"
    ms.author="igamigo"
    displayOrder=""
    articleId="cache-diagnostics-networkinginsight"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="14783"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="RedisCache_RedisCache"
/>

# **Instances of high networking usage detected on the Azure Cache for Redis**

<!--issueDescription-->
Our diagnostics show there were instances where the measurements for "Cache Write" or "Connected Clients" to this Azure Cache for Redis were above critical thresholds when analyzing from **<!--$StartTime-->StartTime<!--/$StartTime-->** to **<!--$EndTime-->EndTime<!--/$EndTime-->**.

Using a high percentage of network writes could cause client requests to time out because the server can't push data fast enough.
This could lead to slower responses and timeouts on the client applications. 
<!--/issueDescription-->

**What can cause high networking usage on an Azure Cache for Redis resource?**

* The load pattern is network intensive, in which case the consistent spikes are expected

## **Recommended Steps**

* Review usage patterns for requests and connections. Avoid creating and closing connections frequently.
* [Create alerts](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-monitor#alerts) on metrics like cache read or cache write to be notified early about potential impacts
**If it's expected due to the kind of data or user pattern, then it's recommended resize to higher Azure Cache for Redis SKU**. You can read more about different [service offerings](https://azure.microsoft.com/pricing/details/virtual-machines/series/) and decide on which one best suits your workload.

## **Recommended Documents**

* [Troubleshooting server-side limitations](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-server#server-side-bandwidth-limitation)
* [Azure Cache for Redis benchmarks](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-management-faq#how-can-i-benchmark-and-test-the-performance-of-my-cache)
