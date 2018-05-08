<properties
	pageTitle="My App is performing slow"
	description="My App is performing slow"
	service="microsoft.cache"
	resource="redis"
	authors="kasparks"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="MoonCake"
/>

# My App is performing slow

## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.

1. Ensure that Redis server is not exceeding the limits for the Cache (exceeding server load, bandwidth, memory limits on the server).<br>
[Diagnosing server-side issues](https://gist.github.com/JonCole/9225f783a40564c9879d)
2. Are you running expensive operations or large values?<br>
[Learn how certain commands can impact performance](https://docs.azure.cn/redis-cache/cache-faq#what-are-some-of-the-considerations-when-using-common-redis-commands)

## **Recommended documents**
[What Redis Cache offering and size should I use?](https://docs.azure.cn/redis-cache/cache-faq#what-redis-cache-offering-and-size-should-i-use)
