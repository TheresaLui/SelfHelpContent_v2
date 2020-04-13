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
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="ffd485ff-828e-4d8b-842c-a5a5cc5e873f"
	ownershipId="Compute_AppService"
/>

#  Performance/HTTP Functions Scaling

## **Recommended Steps**

There are a few configuration knobs you can use to control throughput and concurrency for your http functions. These settings need to go inside an "http" section: <br>

* maxOutstandingRequests 
* maxConcurrentRequests
* dynamicThrottlesEnabled

## **Recommended Documents**

* [HTTP Function Throttling](https://github.com/Azure/azure-functions-host/wiki/Http-Functions#throttling)<br>
