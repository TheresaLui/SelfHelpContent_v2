<properties
	pageTitle="Microsoft Graph authorization failures"
	description="Microsoft Graph authorization failures"
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

# Microsoft Graph authorization failures

Authorization failures can be a result of several different issues. Your app's [authentication flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-scenarios), configured [scopes](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes), and [consent](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent) can influence authorization failures. This article highlights common authorization failures.

## Understanding user and administrator consent for your apps

[How to sign in any Azure Active Directory (AD) user using the multi-tenant application pattern](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)<br>
[Scopes, permissions, and consent in the Azure Active Directory v2.0 endpoint](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes)<br>
[Deciding between the Azure AD and Azure AD v2.0 endpoints](https://developer.microsoft.com/graph/docs/authorization/auth_overview#deciding-between-the-azure-ad-and-azure-ad-v20-endpoints)

## How do my apps get access to customer data using consent? What is a multi-tenant app?

[How to sign in any Azure Active Directory (AD) user using the multi-tenant application pattern](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)

## Choosing required permissions for your app

[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph permission scopes](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## I get a 403 forbidden, but I selected all permissions

For delegated interactive code flows, Microsoft Graph evaluates if the request is allowed based on the permissions granted to the app and the permissions that the user has.  A 403 forbidden error indicates that the user is not privileged enough to perform the request.  Only users with the required permissions will be able to make the request successfully.

[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph permission scopes](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## What do I do when I get a 401 unauthorized error, even though I selected all the permissions?

* If you grant application permissions but use the delegated interactive code flow to acquire a token, you may receive an unauthorized error. If you are granting application permissions to your app, use client credentials daemon service-to-service flow to acquire token.<br>
[Azure Active Directory v2.0 and the OAuth 2.0 client credentials flow](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-protocols-oauth-client-creds)<br>
* If you grant delegated permissions but use the client credentials daemon service-to-service flow to acquire a token, you may receive an unauthorized error. If you are granting delegated permissions to your app, use delegated interactive code flow to acquire token.<br>
[Using OAuth 2.0 Authorization Code Grant for delegated access of Directory via AAD Graph](https://blogs.msdn.microsoft.com/aadgraphteam/2013/05/16/using-oauth-2-0-authorization-code-grant-for-delegated-access-of-directory-via-aad-graph/)

[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph permission scopes](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)

## I configured the app in my tenant with the permissions it needs, but I still get a 401 unauthorized error when trying to use it

1. On your web client application’s configuration page in the Azure portal, set the permissions your application requires by using the menus in the **Required Permissions** section.<br>
2. When the app authenticates to Azure AD if consent has not already been granted, Azure AD will prompt the user for consent and will display the required permissions it needs to function.
3. Administrators can consent to an application's delegated permissions on behalf of all the users in the tenant. An administrator can do this from the Azure portal. From the **Settings** blade for the application, click **Required Permissions** and click on the **Grant Permissions** button.

[Overview of the consent framework](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications#overview-of-the-consent-framework)<br>
[Integrating applications with Azure Active Directory](https://docs.microsoft.com/azure/active-directory/develop/active-directory-integrating-applications)

## I tried to delete users or reset passwords but I get a 401 unauthorized

The application is using daemon service-to-service permissions that do not support these highly privileged operations today.  Please use the interactive code flows with a signed-in administrator.

[Microsoft Graph permission scopes](https://developer.microsoft.com/graph/docs/authorization/permission_scopes)<br>
[Azure AD Graph permission scopes](https://msdn.microsoft.com/library/azure/ad/graph/howto/azure-ad-graph-api-permission-scopes)
