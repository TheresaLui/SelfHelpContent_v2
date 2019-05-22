<properties
	pageTitle="Invalid or Misconfigured Redirect (Reply) URI"
	description="The application has tried a request with a redirect uri that is different than the one configured on the Azure portal."
	infoBubbleText="Found recent login failures. See details on the right."
	service="microsoft.aad"
	resource="MICROSOFT_AAD_IAM"
	authors="abhidnya13"
	ms.author="abpati"
	articleId="active-directory-application-redirecturi-misconfigured"
	diagnosticScenario="MisconfiguredRedirectUri"
	selfHelpType="diagnostics"
	supportTopicIds="32570266,32596845,32596846,32596844,32570262,32596835,32596874,32570261,32596864,32596861"
	resourceTags="appdev"
	productPesIds="16575"
	cloudEnvironments="public"
/>

# <-- Invalid or Misconfigured Redirect (Reply) URI -->

<!--issueDescription-->
The application has tried a request with a Redirect URI (Reply URL) that is different than the one configured on the Azure portal. The details of the request made are as follows: <br><br> Client(Application) Id: **<!--$applicationId-->[applicationId]<!--/$applicationId-->** <br> Timestamp: **<!--$envTime-->[envTime]<!--/$envTime-->** <br> Redirect (Reply) URI (from request): **<!--$redirectURI-->[redirectURI]<!--/$redirectURI-->**
<!--/issueDescription-->

## **Recommended Steps**

1. Open **Azure Portal** and navigate to **Azure Active Directory**
2. From here go to [App registrations (Preview)](https://aka.ms/appregistrations) and select the application facing this issue
3. Navigate to **Authentication**
4. Make sure the **Redirect URI** configured for your application is same as that mentioned above
