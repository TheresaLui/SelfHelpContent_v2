<properties
    pageTitle="Instances of high response sizes were detected"
    description="Instances of metrics near the capacity limits detected"
    infoBubbleText="Instances of metrics near the capacity limits detected"
    service="microsoft.cache"
    resource="redis"
    authors="igamigo"
    ms.author="igamigo"
    displayOrder=""
    articleId="cache-diagnostics-responsesize"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="14783"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="RedisCache_RedisCache"
/>

# **Instances of High Response Size detected**

<!--issueDescription-->
After analyzing the resource usage from **<!--$StartTime-->StartTime<!--/$StartTime-->** to **<!--$EndTime-->EndTime<!--/$EndTime-->**, our diagnostics show there were instances of high response sizes. 

Large requests can cause timeout errors depending on what timeout value was selected and how fast client applications consume the incoming data. 
<!--/issueDescription-->

**What can cause High Response Sizes on an Azure Cache for Redis resource?**

* Having average value sizes be high can cause high response sizes
* Low available bandwidth on the client or the service
* Low client resources could cause timeouts when response sizes are high relative to the read speed. For instance, High client CPU usage indicates the system might not be able to keep up with the work it's been asked to do even if the cache sent the response quickly.

## **Recommended Steps**

**There are several possible changes you can make to help keep response sizes healthy:**

* Redis is optimized for smaller values, so splitting the data into multiple keys will help in avoiding this scenario
* Investigate client VM resources (such as high CPU usage) in order to check whether the client is being slow to read.
* Increase the number of connections that your application uses, making use of a round-robin approach to get good average usage
* [Create alerts](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-monitor#alerts) on metrics like used memory to be notified early about potential impacts

**If this kind of client usage is expected due to the kind of data or user pattern, resizing to a higher Azure Cache for Redis SKU is an alternative**. You can read about different [Azure Cache for Redis offerings](https://azure.microsoft.com/pricing/details/cache/) and decide on which offering best suits your workload.

## **Recommended Documents**

* [Troubleshoot Azure Cache for Redis client-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client#large-request-or-response-size)
* [How to monitor Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-monitor#available-metrics-and-reporting-intervals)
* [Best practices for Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-best-practices)
