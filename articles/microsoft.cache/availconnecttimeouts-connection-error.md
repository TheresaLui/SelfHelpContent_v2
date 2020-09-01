<properties
	pageTitle="Connection errors with Azure Cache for Redis"
	description="Connection errors with Azure Cache for Redis"
	service="microsoft.cache"
	resource="redis"
	authors="asasine"
	ms.author="adsasine"
	displayOrder="21"
	selfHelpType="resource"
	supportTopicIds="32690905"
	resourceTags=""
	productPesIds="14783"
	cloudEnvironments="public,blackForest,fairfax,mooncake, usnat, ussec"
	articleId="8e369a6b-0ed1-4419-8b1c-a2cb320219bf"
	ownershipId="RedisCache_RedisCache"
/>

# Connection errors with Azure Cache for Redis

Applications may receive connection errors when the client is unable to establish a TCP connection with Redis server. These may surface as runtime connection exceptions or errors. Separate from connection errors, timeout errors from failed requests or commands may indicate a different problem. Use the recommended documents below to investigate and resolve connection errors.

## **Recommended Documents**

* [Troubleshoot Azure Cache for Redis server-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-server)<br>
* [Troubleshoot Azure Cache for Redis client-side issues](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-troubleshoot-client)<br>
* [TLS 1.0 and 1.1 are being retired](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-remove-tls-10-11)<br>
* [VNET FAQ](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-how-to-premium-vnet#azure-cache-for-redis-vnet-faq)<br>
* [Best practices for Azure Cache for Redis](https://docs.microsoft.com/azure/azure-cache-for-redis/cache-best-practices)
