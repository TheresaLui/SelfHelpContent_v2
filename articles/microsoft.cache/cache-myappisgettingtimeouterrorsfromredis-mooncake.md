<properties
	pageTitle="My app is getting timeout errors from Redis"
	description="My app is getting timeout errors from Redis"
	service="microsoft.cache"
	resource="redis"
	authors="kasparks"
	displayOrder="3"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# My app is getting timeout errors from Redis

## **Recommended steps**
Try following steps to diagnose and mitigate timeout errors.

1. Common reasons for timeouts are- lack of available free memory, high Redis server load, low on network bandwidth capacity or large request/response size. Use following article to diagnose and resolve these issues.<br>
[Troubleshoot timeout issues](https://gist.github.com/JonCole/db0e90bedeb3fc4823c2)
2. Certain timeout errors can be resolved by upgrading to a Cache with better performance, more memory, network bandwidth and number of connected clients.

## **Recommended documents**
[What Redis Cache offering and size should I use?](https://docs.azure.cn/redis-cache/cache-faq#what-redis-cache-offering-and-size-should-i-use)
