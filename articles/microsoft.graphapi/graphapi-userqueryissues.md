<properties
	pageTitle="Microsoft Graph querying or provisioning issues"
	description="Information about querying or provisioning issues using Microsoft Graph APIs."
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="davidmu1"
	ms.author="davidmu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689193,32134055"
	resourceTags=""
	productPesIds="16953,16575"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="757bafde-f257-47fe-9114-2b24c5bf4ac9"
	ownershipId="AzureIdentity_GraphUsersAndGroupsAPIs"
/>

# Microsoft Graph querying or provisioning issues

This topic may also apply to developers still using Azure AD Graph API. However, it is **strongly** recommended that you use Microsoft Graph for all your directory, identity, and access management scenarios.

## **Recommended steps**

Check the answers already available in Stack Overflow for [Azure AD questions in Microsoft Graph](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+Azure+AD+isanswered%3Ayes+views%3A50), or craft your own more specific search query. If you can't find a solution to your problem, [ask a new question on Stack Overflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

**Authentication or authorization issues**

* If your app is **unable to acquire tokens** to call Microsoft Graph, pick **Problem with getting an access token (Authentication)** Microsoft Graph category to get more specific help and support on this topic
* If your app is **receiving 401 or 403 authorization errors** when calling Microsoft Graph, pick the **Getting an access denied error (Authorization)** Microsoft Graph API category to get more specific help and support on this topic

**I want to use Microsoft Graph, but not sure where to start**

* [Overview of Microsoft Graph](https://developer.microsoft.com/graph/docs)
* [Overview of Identity and Access Management in Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/azuread-identity-access-management-concept-overview)
* [Getting started building Microsoft Graph apps](https://developer.microsoft.com/graph/docs/get-started/get-started)
* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://developer.microsoft.com/graph/graph-explorer) 

**I want to use Microsoft Graph, but does it support the v1.0 directory APIs I need?** <br>

Microsoft Graph is the recommended API for directory, identity, and access management. However, there are still a few gaps between what is possible in Azure AD Graph and Microsoft Graph. Review the following articles, which highlight the most up-to-date differences to assist in your choice:

* [Resource type differences between Azure AD Graph and Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-resource-differences)
* [Property differences between Azure AD Graph and Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-property-differences)
* [Method differences between Azure AD and Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-method-differences)

**When I query the *user* object, many of its properties are missing**

*GET https://graph.microsoft.com/v1.0/users* only returns 11 properties, as Microsoft Graph auto-selects a default set of *user* properties to return. If you need other *user* properties, use $select to pick the properties your application needs. Try it out in [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer) first.

**Some user property values are *null* even though I know they are set** 

The most likely explanation is that the application had been granted the *User.ReadBasic.All* permission. This allows the application to read a limited set of user properties, returning all other properties as null even if they have been previously set. Try granting the application *User.Read.All* permission instead.

* [Microsoft Graph user permissions](https://developer.microsoft.com/graph/docs/concepts/permissions_reference#user-permissions) <br>

**I'm having trouble using OData query parameters to filter data in my requests** 

While Microsoft Graph supports a wide range of the OData query parameters, many of those parameters are not fully supported by directory services (resources that inherit from *directoryObject*) in Microsoft Graph. The same limitations that were present in Azure AD Graph persist for the most part in Microsoft Graph:

1. **Not supported**: $count, $search, and $filter on *null* or *not* *null* values
2. **Not supported**: $filter on certain properties (see resource topics on which properties are filterable)
3. **Not supported**: paging, filtering, and sorting at the same time
4. **Not supported**: filtering on a relationship. For example - find all members of the engineering group that are in the UK.
5. **Partial support**: $orderby on *user* (displayName and userPrincipalName only) and *group*
6. **Partial support**: $filter (supports only *eq*, *startswith*, *or*, *and*, and limited *any*) support, $expand (expanding a single object's relationships returns all relationships, but expanding a collection of objects' relationships is limited)

* [Customize responses with query parameters](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters)

**The API I'm calling doesn't work - where can I do more testing?**

* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://developer.microsoft.com/graph/graph-explorer). Also, check out the **sample queries** in Microsoft Graph Explorer. 

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
