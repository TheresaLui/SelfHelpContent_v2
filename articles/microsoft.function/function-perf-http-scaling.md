<properties
	pageTitle="Performance/HTTP Functions Scaling"
	description="Performance/HTTP Functions Scaling"
	service="microsoft.web"
	resource="functions"
	authors="cts-shrahman,shrahman"
    ms.author="shrahman,ykchen"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32630475"
	resourceTags=""
	productPesIds="16072"
	cloudEnvironments="public"
/>

#  Performance/HTTP Functions Scaling

## **Recommended steps**

There are a few configuration knobs you can use to control throughput and concurrency for your http functions. These settings need to go inside an "http" section and they are: <br>
* maxOutstandingRequests 
* maxConcurrentRequests
* dynamicThrottlesEnabled


## **Recommended documents**

* [HTTP Function Throttling](https://github.com/Azure/azure-functions-host/wiki/Http-Functions#throttling)<br>
