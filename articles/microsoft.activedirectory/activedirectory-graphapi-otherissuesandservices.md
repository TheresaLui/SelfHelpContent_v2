<properties
	pageTitle="Other Microsoft Graph issues"
	description="More information about calling Microsoft Graph APIs and some of the common problems that developers encounter."
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="dkershaw10"
	ms.author="dkershaw"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596860"
	resourceTags=""
	productPesIds="16575"
	cloudEnvironments="public"
	articleId="86ac72d1-45ca-4c70-a865-37d5550a6f87"
/>

# Other Microsoft Graph Issues

If none of the other support topic categories quite fit your issue, please read on or try picking a different support category.

## **Recommended Steps**

Check the answers already available in StackOverflow for [Microsoft Graph](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+isanswered%3Ayes+views%3A50) or craft your own, more specific search query. If you can't find a solution to your problem, [ask a new question on StackOverflow](https://stackoverflow.com/questions/ask) and tag with  *microsoft-graph*.

**Authentication or Authorization Issues**

* If your app is **unable to acquire tokens** to call Microsoft Graph, pick the **Authentication token issues** Graph API category to get more specific help and support on this topic
* If your app is **receiving authorization errors** when calling Microsoft Graph, pick the **Authentication token issues** Graph API category to get more specific help and support on this topic

**I have an issue with a different service or API that doesn't have a support category** 

You can find more information on some of the other services and features in Microsoft Graph:

* [Major services and features in Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/overview-major-services) 
* [Microsoft Graph API v1.0 reference documentation](https://developer.microsoft.com/graph/docs/concepts/v1-overview)
* [Microsoft Graph API beta reference documentation](https://developer.microsoft.com/graph/docs/api-reference/beta/beta-overview)

**The API I'm calling doesn't work - where can I do more testing?**

* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://aka.ms/ge). Also, check out the **sample queries** in Microsoft Graph Explorer. 

**When I query for data it seems like I get an incomplete data set back**

If you are querying a collection (like *users*), Microsoft Graph uses server-side page limits so result are always returned with a default page-size. Your app should always expect to page through collections returned from the service.

* [Microsoft Graph best practices](https://developer.microsoft.com/graph/docs/concepts/best-practices-concept)
* [Paging Microsoft Graph data in your app](https://developer.microsoft.com/graph/docs/concepts/paging)

**My app is too slow and is also getting throttled. What improvements can I make?**

Depending on your scenario, there are a variety of different options at your disposal to make your application more performant, and in some cases, less prone to being throttled by the service (when you are making too many calls).

* [Microsoft Graph best practices](https://developer.microsoft.com/graph/docs/concepts/best-practices-concept) 
* [Batching requests](https://developer.microsoft.com/graph/docs/concepts/json_batching) 
* [Track changes through delta query](https://developer.microsoft.com/graph/docs/concepts/delta_query_overview) 
* [Get notified of changes through webhooks](https://developer.microsoft.com/graph/docs/concepts/webhooks)
* [Throttling guidance](https://developer.microsoft.com/graph/docs/concepts/throttling)

**Where can I find more information on errors and known issues?** 

* [Microsoft Graph error response information](https://developer.microsoft.com/graph/docs/overview/errors)
* [Known issues with Microsoft Graph](https://developer.microsoft.com/graph/docs/overview/release_notes)

**Where can I check status of service availability and connectivity?**

The service availability and connectivity of the underlying services that can be accessed through Microsoft Graph can impact the overall availability and performance of Microsoft Graph.

* For Azure Active Directory service health, check the status of **Security + Identity** services listed in the [Azure status page](https://azure.microsoft.com/status/)
* For Office services that contribute to Microsoft Graph, check the status of services listed in the [Office Service Health Dashboard](https://portal.office.com/adminportal/home#/servicehealth)

**I'm having trouble using OData query parameters to filter data in my requests**

While Microsoft Graph supports a wide range of the OData query parameters, many of those parameters are not fully supported across all the services within Microsoft Graph.

* [Customize responses with query parameters](https://developer.microsoft.com/graph/docs/concepts/query_parameters) 
