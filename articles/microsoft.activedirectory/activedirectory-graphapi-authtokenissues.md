<properties
	pageTitle="Microsoft Graph authentication token issues"
	description="Microsoft Graph authentication token issues"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134055"
	resourceTags=""
	productPesIds="14785,16575"
	cloudEnvironments="public"
/>

# Microsoft Graph authentication token issues

## How do I authenticate and authorize Graph APIs?

To get your app authorized, you authenticate the user first. You do this by redirecting the user to the Azure Active Directory (Azure AD) authorization endpoint, along with your app information, to sign in to their work or school account. Once the user is signed in, and consents to the permissions requested by your app (if the user has not done so already), your app will receive an authorization code required to acquire an OAuth access token.

[Microsoft Graph app authentication using Azure AD](https://developer.microsoft.com/graph/docs/authorization/app_authorization)

## How do I call Microsoft Graph from a daemon service where there is no user signed-in?

For service or daemon apps, your application should implement the OAuth 2.0 Client Credentials Grant Flow. Instead of impersonating a user, the app uses its own credentials, client ID, and application key to authenticate when calling the Microsoft Graph.

[Call Microsoft Graph in a service or daemon app](https://developer.microsoft.com/graph/docs/authorization/app_only)
