<properties
	pageTitle="My app is getting connectivity errors"
	description="My app is getting connectivity errors"
	service="microsoft.cache"
	resource="redis"
	authors="kasparks"
	displayOrder="2"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
	articleId="9d32fc66-40fb-4f4c-b9d8-9848deac69b0"
/>

# My app is getting connectivity errors

## **Recommended steps**
To resolve the most common issues, try one or more of the following methods.

1. Use recommended client configuration for your platform.<br>
[List of recommended Redis clients by language](http://redis.io/clients)
2. Check if you are exceeding the maximum number of client connections.<br>
[Learn about limits for number of client connections](http://aka.ms/redistroubleshoortfaq)
3. If hosted on Azure Virtual Network (VNet), check the ports are not blocked.<br>
[Common misconfiguration issues with Redis Cache and VNet](http://aka.ms/redistroubleshootvnet)
4. Were you scaling out your client app? While scaling out there can be momentarily loss of connectivity. The clients should reconnect after the scale operation has finished.

## **Recommended documents**
[What Redis Cache offering and size should I use?](http://aka.ms/redistroubleshootoffering)
