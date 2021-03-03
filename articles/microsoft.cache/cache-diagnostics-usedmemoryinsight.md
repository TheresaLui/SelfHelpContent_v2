<properties
    pageTitle="Instances of high memory usage detected"
    description="Instances of metrics near the capacity limits detected"
    infoBubbleText="Instances of metrics near the capacity limits detected"
    service="microsoft.cache"
    resource="redis"
    authors="igamigo"
    ms.author="igamigo"
    displayOrder=""
    articleId="cache-diagnostics-usedmemoryinsight"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="14783"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="RedisCache_RedisCache"
/>

# **Instances of High Memory Pressure detected**

<!--issueDescription-->
After analyzing the resource usage on **<!--$ResourceName-->ResourceName<!--/$ResourceName-->** from **<!--$StartTime-->StartTime<!--/$StartTime-->** to **<!--$EndTime-->EndTime<!--/$EndTime-->**, our diagnostics show there were instances of high memory pressure. 

When the used memory of the service is close to or exceeding the limits, the system may page data to disk (page faulting) which could lead to unavailability or timeouts on the client applications. 
<!--/issueDescription-->

**What can cause Memory Pressure on an Azure Cache for Redis resource?**

* The Azure Cache for Redis resource is high on memory usage and is close to its maximum capacity
* The service is experiencing high memory fragmentation

## **Recommended Steps**

**There are several possible changes you can make to help keep memory usage healthy:**

* Configure a [memory policy](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-configure#maxmemory-policy-and-maxmemory-reserved) and set expiration times on your keys. This policy may not be sufficient if you have fragmentation
* Configure a [maxmemory-reserved](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-configure#maxmemory-policy-and-maxmemory-reserved) value that is large enough to compensate for memory fragmentation
* Review the "Page Faults/Sec" performance counter. Spikes in page faults corresponding with request timeouts can indicate memory pressure.
* Break up your large cached objects into smaller related objects
* [Create alerts](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-monitor#alerts) on metrics like used memory to be notified early about potential impacts

**If this kind of memory usage is expected due to the kind of data or user pattern, then it is recommended to resize to higher Azure Cache for Redis SKU**. You can read about different [Azure Cache for Redis offerings](https://azure.microsoft.com/pricing/details/cache/) and decide on which one best suits your workload.

## **Recommended Documents**

* [Troubleshoot Azure Cache for Redis client-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client)
* [How to monitor Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-monitor#available-metrics-and-reporting-intervals)
* [Monitoring and troubleshooting FAQ](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-monitor-troubleshoot-faq)
