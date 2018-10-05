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

## **Recommended steps**

You can check the answers already available in StackOverflow for [Microsoft Graph and authentication](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+authentication+isanswered%3Ayes+views%3A50) or craft your own, more specific search query. If you can't find a solution to your problem, [ask a new question on StackOverflow](https://stackoverflow.com/questions/ask) and tag with  `microsoft-graph`.

**How do I authenticate and get an access token to Microsoft Graph?**

To get your app authorized, you authenticate the user first. You do this by redirecting the user to the Azure Active Directory (Azure AD) authorization endpoint, along with your app information, to sign users in to their work or school account. Once the user is signed in, and consents to the permissions requested by your app (if the user has not done so already), your app will receive an authorization code that can be redeemed for an OAuth access token.  You might also have a cached refresh token that can also be redeemed for an OAuth access token

[Call Microsoft Graph on behalf of the signed-in user](https://developer.microsoft.com/graph/docs/concepts/auth_v2_user) <br>

**How do I call Microsoft Graph from a daemon service where there is no user signed-in?**

For service or daemon apps, your application should implement the OAuth 2.0 Client Credentials Grant Flow. Instead of impersonating a user, the app uses its own credentials, client ID, and application key to authenticate when calling the Microsoft Graph.

[Call Microsoft Graph in a service or daemon app](https://developer.microsoft.com/graph/docs/authorization/app_only) <br>

