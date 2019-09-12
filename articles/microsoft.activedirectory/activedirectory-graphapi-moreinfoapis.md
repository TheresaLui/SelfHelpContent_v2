<properties
	pageTitle="Calling Microsoft Graph directory APIs"
	description="More information about calling Microsoft Graph directory APIs and some of the common problems that developers encounter."
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="dkershaw10"
	ms.author="dkershaw"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32596839,32596852"
	resourceTags=""
	productPesIds="16575"
	cloudEnvironments="public"
	articleId="0eeff0ad-b53b-4e1a-a9ac-e7a0b7db502d"
/>

# Calling Microsoft Graph directory APIs

This topic may also apply to developers still using Azure AD Graph API. However, it is **strongly** recommended that you use Microsoft Graph for all your directory, identity, and access management scenarios.

## **Recommended Steps**

Check the answers already available in StackOverflow for [Azure AD questions in Microsoft Graph](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+Azure+AD+isanswered%3Ayes+views%3A50), or craft your own more specific search query. If you can't find a solution to your problem, [ask a new question on StackOverflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

**Authentication or Authorization Issues**

* If your app is **unable to acquire tokens** to call Microsoft Graph, pick the **Authentication token issues** Graph API category to get more specific help and support on this topic
* If your app is **receiving authorization errors** when calling Microsoft Graph, pick the **Authentication token issues** Graph API category to get more specific help and support on this topic

**I want to use Microsoft Graph, but not sure where to start**

* [Overview of Microsoft Graph](https://developer.microsoft.com/graph/docs)
* [Overview of Identity and Access Management in Microsoft Graph](https://developer.microsoft.com/graph/docs/concepts/azuread-identity-access-management-concept-overview)
* [Getting started building Microsoft Graph apps](https://developer.microsoft.com/graph/docs/get-started/get-started)
* [Microsoft Graph Explorer - Test Microsoft Graph APIs in your tenant or a demo tenant](https://aka.ms/ge) 

**I want to use Microsoft Graph, but does it support the GA directory APIs I need?** <br>

Microsoft Graph is the recommended API for directory, identity, and access management. However, there are still a few gaps between what is possible in Azure AD Graph and Microsoft Graph. Review the following article, which highlights these differences for you to assist in your choice:

* [Choosing between Microsoft Graph or Azure AD Graph](https://developer.microsoft.com/office/blogs/microsoft-graph-or-azure-ad-graph/)

**When I query the *user* object, many of its properties are missing**

*GET https://graph.microsoft.com/v1.0/users* only returns 11 properties, as Microsoft Graph auto-selects a default set of *user* properties to return. If you need other *user* properties, use $select to pick the properties your application needs. Try it out in [Graph Explorer](https://aka.ms/ge) first.

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
6. **Partial support**: $filter (supports only *eq*, *startswith*, *or*, *and*), $expand (expanding a single object's relationships returns all relationships, but expanding a collection of objects' relationships is limited)

* [Customize responses with query parameters](https://developer.microsoft.com/en-us/graph/docs/concepts/query_parameters)
