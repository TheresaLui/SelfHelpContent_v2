<properties
	pageTitle="Microsoft Graph service performance"
	description="Microsoft Graph service performance"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134062"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# Microsoft Graph service performance

## My application is being throttled

Throttling limits the number of concurrent calls to a service to prevent overuse of resources. Microsoft Graph is designed to handle a very high volume of requests. In the event of an overwhelming number of requests, throttling helps maintain optimal performance and reliability of the Microsoft Graph service. 

Microsoft Graph<br>
Consider [using delta query to track changes in Microsoft Graph data](https://developer.microsoft.com/graph/docs/concepts/delta_query_overview) to reduce the total number of requests by an app. By reducing the total number of requests, your app is less likely to be affected by throttling.

Azure Active Directory Graph<br>
[Azure AD throttling guidance](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)<br>
[Batch processing](https://msdn.microsoft.com/Library/Azure/Ad/Graph/howto/azure-ad-graph-api-batch-processing) is an option reduce the total number of requests. By reducing the total number of requests, your app is less likely to be affected by throttling.

## Where can I find details about the graph API throttle limits?

Throttling behavior can be dependent on the type and number of requests. For example, if you have a very high volume of requests, all requests types are throttled. Threshold limits vary based on the request type. Therefore, you could encounter a scenario where writes are throttled but reads are still permitted. Because many factors can influence throttling behavior, specific throttling limits are not published. 

Microsoft Graph<br>
[Microsoft Graph error responses and resource types](https://developer.microsoft.com/graph/docs/overview/errors)

Azure Active Directory Graph<br>
[Azure AD Graph throttling guidance](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-throttling)