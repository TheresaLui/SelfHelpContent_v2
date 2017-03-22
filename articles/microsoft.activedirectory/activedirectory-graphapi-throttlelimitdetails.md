<properties
	pageTitle="Where can I find details about the Graph API throttle limits"
	description="Where can I find details about the Graph API throttle limits"
	service="microsoft.aad"
	resource=""
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134062"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Where can I find details about the Graph API throttle limits?

Throttling behavior can be dependent on the type and number of requests. For example, if you have a very high volume of requests, all requests types are throttled. Threshold limits vary based on the request type. Therefore, you could encounter a scenario where writes are throttled but reads are still permitted. Because many factors can influence throttling behavior, specific throttling limits are not published.

## **Recommended documents**
[Throttling guidance](https://msdn.microsoft.com/en-us/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)