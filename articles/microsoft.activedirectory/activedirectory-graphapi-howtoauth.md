<properties
	pageTitle="How do I authenticate and authorize Graph APIs"
	description="How do I authenticate and authorize Graph APIs"
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

# How do I authenticate and authorize Graph APIs?

To get your app authorized, you authenticate the user first. You do this by redirecting the user to the Azure Active Directory (Azure AD) authorization endpoint, along with your app information, to sign in to their work or school account. Once the user is signed in, and consents to the permissions requested by your app (if the user has not done so already), your app will receive an authorization code required to acquire an OAuth access token.

## **Recommended documents**
[Microsoft Graph app authentication using Azure AD](https://developer.microsoft.com/graph/docs/authorization/app_authorization)