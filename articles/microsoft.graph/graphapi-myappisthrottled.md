<properties
	pageTitle="My application is being throttled"
	description="My application is being throttled"
	service="Microsoft.graph"
	resource="resourceName"
	authors="PatAltimore"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags="optional"
	productPesIds=""
	cloudEnvironments="public"
/>

# My application is being throttled

Throttling limits the number of concurrent calls to a service to prevent overuse of resources. Microsoft Graph is designed to handle a very high volume of requests. In the event of an overwhelming number of requests, throttling helps maintain optimal performance and reliability of the Microsoft Graph service.

## **Recommended steps**
* Reduce the number of operations per request.
* Reduce the frequency of calls.
* When requests fail with a HTTP error code 429, wait the number of seconds specified in the Retry-After response header field and retry the request.
* Use delta query to synchronize changes with a local data store.<br>
[Use delta query to track changes in Microsoft Graph data](https://developer.microsoft.com/en-us/graph/docs/concepts/delta_query_overview)
* Use batch operations to reduce roundtrips to the server.<br>
[Batch processing](https://msdn.microsoft.com/en-us/Library/Azure/Ad/Graph/howto/azure-ad-graph-api-batch-processing)


## **Recommended documents**
[Throttling guidance](https://msdn.microsoft.com/en-us/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)