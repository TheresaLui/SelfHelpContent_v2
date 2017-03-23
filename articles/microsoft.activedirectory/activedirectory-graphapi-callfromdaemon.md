<properties
	pageTitle="How do I call Microsoft Graph from a daemon service where there is no user signed-in"
	description="How do I call Microsoft Graph from a daemon service where there is no user signed-in"
	service="microsoft.aad"
	resource="Microsoft_AAD_IAM"
	authors="PatAltimore"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32134055"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>

# How do I call Microsoft Graph from a daemon service where there is no user signed-in?

For service or daemon apps, your application should implement the OAuth 2.0 Client Credentials Grant Flow. Instead of impersonating a user, the app uses its own credentials, client ID, and application key to authenticate when calling the Microsoft Graph.

## **Recommended documents**
[Call Microsoft Graph in a service or daemon app](https://developer.microsoft.com/graph/docs/authorization/app_only)