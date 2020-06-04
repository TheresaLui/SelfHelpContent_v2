<properties
	pageTitle="Microsoft Graph authentication token issues"
	description="Microsoft Graph authentication token issues"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="davidmu1"
	ms.author="davidmu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32689192,32596860"
	resourceTags=""
	productPesIds="16952,16575"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	articleId="2e5a474e-839f-432d-8bf3-7ed39d7635c3"
	ownershipId="AzureIdentity_MSGraph"
/>

# Microsoft Graph authentication token issues

This topic deals with failures to acquire access tokens to call Microsoft Graph. These issues may also be related to any failure to grant consent to access Microsoft Graph, for your application.

## **Recommended Steps**

Check the answers already available in Stack Overflow for [Microsoft Graph and authentication](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+authentication+isanswered%3Ayes+views%3A50), or craft your own, more specific search query. If you can't find a solution to your problem, [ask a new question on Stack Overflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

We strongly recommend the use of the [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/msal-overview) to acquire access tokens to call Microsoft Graph.

Review [Authentication flows and application scenarios](https://docs.microsoft.com/azure/active-directory/develop/authentication-flows-app-scenarios#scenarios-and-supported-platforms-and-languages) to see which scenario your application falls under, and follow the token acquisition guidance, language/platform support, and samples for that scenario. This represents the most comprehensive list, but the two most common scenarios are also described below.

**How do I authenticate and get an access token to Microsoft Graph?**

To authorize your app, authenticate the user first. You do this by redirecting the user to the Azure Active Directory (Azure AD) authorization endpoint, along with your app information, to sign users in to their work or school account, or their personal Microsoft account. After the user signs in and consents to the permissions requested by your app (if the user has not done so already), your app receives an authorization code that can be redeemed for an OAuth2.0 access token. You might also have a cached refresh token that you can redeem for an OAuth access token.

* [Call Microsoft Graph on behalf of the signed-in user](https://developer.microsoft.com/graph/docs/concepts/auth_v2_user)

**How do I call Microsoft Graph from a daemon service where there is no user signed-in?**

For service or daemon apps, your application should implement the OAuth 2.0 Client Credentials Grant Flow. Instead of impersonating a user, the app uses its own credentials, client ID, and application key to authenticate when calling the Microsoft Graph.

* [Call Microsoft Graph in a service or daemon app](https://developer.microsoft.com/graph/docs/authorization/app_only) 

**How do I get more information about AADSTS error codes?**

For more information, see [Authentication and authorization error codes](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes).

## **Recommended Documents**

* [I am seeing trouble signing in to application(s) using Chrome browser only](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications)
