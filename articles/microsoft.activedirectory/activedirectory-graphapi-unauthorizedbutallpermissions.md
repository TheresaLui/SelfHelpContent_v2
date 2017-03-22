<properties
	pageTitle="What do I do when I get a 401 unauthorized error, even though I selected all the permissions"
	description="What do I do when I get a 401 unauthorized error, even though I selected all the permissions"
	service="microsoft.aad"
	resource=""
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134056"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# What do I do when I get a 401 unauthorized error, even though I selected all the permissions?

## **Recommended steps**
* If using application permissions, use client credentials daemon service-to-service flow to acquire token.<br>
[Azure Active Directory v2.0 and the OAuth 2.0 client credentials flow](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)<br>
* If using delegated permissions, use delegated interactive code flow to acquire token.<br>
[Using OAuth 2.0 Authorization Code Grant for delegated access of Directory via AAD Graph](https://blogs.msdn.microsoft.com/aadgraphteam/2013/05/16/using-oauth-2-0-authorization-code-grant-for-delegated-access-of-directory-via-aad-graph/)

## **Recommended documents**
[Microsoft Graph permission scopes](https://developer.microsoft.com/en-us/graph/docs/authorization/permission_scopes)<br>
[Permission scopes | Graph API concepts](https://msdn.microsoft.com/en-us/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)