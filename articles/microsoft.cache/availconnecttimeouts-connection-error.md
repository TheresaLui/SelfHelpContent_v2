<properties
	pageTitle="Connection errors with Azure Cache for Redis"
	description="Connection errors with Azure Cache for Redis"
	service="microsoft.cache"
	resource="redis"
	authors="asasine"
	ms.author="adsasine"
	displayOrder="21"
	selfHelpType="generic"
	supportTopicIds="32690905"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="8e369a6b-0ed1-4419-8b1c-a2cb320219bf"
	ownershipId="RedisCache_RedisCache"
/>

# Connection errors with Azure Cache for Redis

Applications can receive connection error messages when the client is unable to establish a TCP connection with the Redis server. These error messages can surface as runtime connection exceptions or as errors. Separate from connection errors, timeout errors from failed requests or commands can indicate a different problem. 

Use the following recommended documents to investigate and resolve connection errors.

## **Recommended Documents**

* [Common causes of connection errors and how to fix them](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client)<br>
* [What is failover and how to make clients resilient to failover ](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-failover)<br>
* [How does patching occur and how to make clients resilient to patching](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-failover#how-does-patching-occur)<br>
* [Common configuration issues within VNET that causes connection errors](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-premium-vnet#azure-cache-for-redis-vnet-faq)<br>
* [Best practices for better performance and reducing errors](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-best-practices)<br>
* [Remove TLS 1.0 and 1.1](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-remove-tls-10-11)<br>
* [Troubleshoot server side issues that causes connection errors](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-server)<br>
* [Common causes for data loss](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-data-loss)<br>
* [Azure Cache for Redis complete documentation](https://docs.microsoft.com/azure/azure-cache-for-redis/)
