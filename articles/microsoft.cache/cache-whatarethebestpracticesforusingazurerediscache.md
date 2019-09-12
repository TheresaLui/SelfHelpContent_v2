<properties
	pageTitle="What are the best practices for using Azure Redis Cache?"
	description="What are the best practices for using Azure Redis Cache?"
	service="microsoft.cache"
	resource="redis"
	authors="kasparks"
	displayOrder="4"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="aa0654f6-59a7-418f-aba3-13ecd9e1cf50"
/>

# What are the best practices for using Azure Redis Cache?

## **Recommended steps**
To learn more about best practices, try one or more of the following.

1. Use the latest version of the client library for your application.<br>
[List of Redis clients by language](http://redis.io/clients)
2. Basic tier is for Dev/test only and there is no SLA. Standard or Premium tier is recommended for production usage.
3. Use Redis data persistence to increase resiliency against potential data loss.<br>
[Learn more about configuring Redis data persistence](https://azure.microsoft.com/documentation/articles/cache-how-to-premium-persistence/)
4. Use the following article to learn more about best practices to improve performance and scalability of cache.<br>
[Learn more best practices](http://aka.ms/redistroubleshootpnp)

## **Recommended documents**
[What Redis Cache offering and size should I use?](http://aka.ms/redistroubleshootoffering)
