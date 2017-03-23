<properties
	pageTitle="What do I do when I get a 401 unauthorized error, even though I selected all the permissions"
	description="What do I do when I get a 401 unauthorized error, even though I selected all the permissions"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
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
* If you grant application permissions but use the delegated interactive code flow to acquire a token, you may receive an unauthorized error. If you are granting application permissions to your app, use client credentials daemon service-to-service flow to acquire token.<br>
[Azure Active Directory v2.0 and the OAuth 2.0 client credentials flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)<br>
* If you grant delegated permissions but use the client credentials daemon service-to-service flow to acquire a token, you may receive an unauthorized error. If you are granting delegated permissions to your app, use delegated interactive code flow to acquire token.<br>
[Using OAuth 2.0 Authorization Code Grant for delegated access of Directory via AAD Graph](https://blogs.msdn.microsoft.com/aadgraphteam/2013/05/16/using-oauth-2-0-authorization-code-grant-for-delegated-access-of-directory-via-aad-graph/)

## **Recommended documents**
[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Permission scopes | Graph API concepts](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)