<properties
	pageTitle="Microsoft Graph querying or provisioning issues"
	description="Information about querying or provisioning issues using Microsoft Graph APIs."
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="davidmu1"
	ms.author="davidmu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689193"
	resourceTags=""
	productPesIds="16954,16955,16956,16575"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="1ab76fd2-7673-4011-b9fe-8ac1335f260c"
	ownershipId="AzureIdentity_GraphMessagesAndContactsAPIs"
/>

# Microsoft Graph querying or provisioning issues

## **Recommended Steps**

Check the answers already available in Stack Overflow for [questions about Microsoft Graph](https://stackoverflow.com/search?tab=newest&q=%5bmicrosoft-graph%5d%20query%20isanswered%3ayes%20views%3a50), or craft your own more specific search query. If you can't find a solution to your problem, [ask a new question on Stack Overflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

**Authentication or authorization issues**

* If your app is **unable to acquire tokens** to call Microsoft Graph, pick **Problem with getting an access token (Authentication)** Microsoft Graph category to get more specific help and support on this topic
* If your app is **receiving 401 or 403 authorization errors** when calling Microsoft Graph, pick the **Getting an access denied error (Authorization)** Microsoft Graph API category to get more specific help and support on this topic

**I want to use Microsoft Graph, but not sure where to start**

* [Overview of Microsoft Graph](https://developer.microsoft.com/graph/docs)
* [Overview of Identity and Access Management in Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/azuread-identity-access-management-concept-overview)
* [Getting started building Microsoft Graph apps](https://developer.microsoft.com/graph/docs/get-started/get-started)
* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://developer.microsoft.com/graph/graph-explorer) 


**The API I'm calling doesn't work - where can I do more testing?**

* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://developer.microsoft.com/graph/graph-explorer). Also, check out the **sample queries** in Microsoft Graph Explorer. 

**When I query for data it seems like I get an incomplete data set back**

If you are querying a collection, Microsoft Graph uses server-side page limits so result are always returned with a default page-size. Your app should always expect to page through collections returned from the service.

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
