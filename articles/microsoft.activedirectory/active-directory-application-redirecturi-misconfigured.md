<properties
	pageTitle="I received an error related to the reply url"
	description="I received an error related to the reply url."
	infoBubbleText="Found recent login failures. See details on the right."
	service="microsoft.aad"
	resource="MICROSOFT_AAD_IAM"
	authors="jmprieur"
	ms.author="jmprieur"
	diagnosticScenario="MisconfiguredRedirectUri"
	selfHelpType="generic"
	supportTopicIds="32596861"
	resourceTags="appdev"
	productPesIds="16575"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="active-directory-application-redirecturi-misconfigured"
	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
/>
# I received an error related to the reply url

Redirect URI/reply URLs (both expressions are interchangeable) are the URL used by the Microsoft identity platform to return app-requested tokens. 

## **Recommended Steps**

### I don't know how to register the right redirect URI / reply URL for my app

When you sign in with the application you are developing, if the sign-in dialog displays `AADSTS50011: The reply url specified in the request does not match the reply urls configured for the application <your app ID>`, you'll need to add to your application registration, the redirect URI that your code used in the token request to the Microsoft identity platform.

To add a reply URL, go to the **Authentication** tab in your application registration, in the Azure portal and add an entry in the **Redirect URIs** section. Redirect URIs are typed (Web or mobile/desktop). The value you need to enter depends on the type of application you're building:  

- For single page applications and web apps, the reply URL is a URL in your application. See [Single-page application registration](https://docs.microsoft.com/azure/active-directory/develop/scenario-spa-app-registration#register-a-redirect-uri) or [Register a web app app using Azure portal](https://docs.microsoft.com/azure/active-directory/develop/scenario-web-app-sign-user-app-registration?tabs=aspnetcore#register-an-app-using-azure-portal)
- For desktop applications the value that you need to choose depends on:
  - the platform (MacOS is different from Windows or Linux)
  - the way you acquire the token (interactively, with device code flow, with integrated Windows authentication or with username/password)
  
For details see [Desktop apps - App registration - Redirect URi](https://docs.microsoft.com/azure/active-directory/develop/scenario-desktop-app-registration#redirect-uris).
  
- For mobile applications, the redirect URI depends on:

  - the platform (iOS/Android/UWP)
  - the information used to build your app such as the bundle ID in iOS, and the package name and signature hash on Android
  
The Azure portal app registration will help you. For details see [Platform configuration and redirect URIs](https://docs.microsoft.com/azure/active-directory/develop/scenario-mobile-app-registration#platform-configuration-and-redirect-uris)

**NOTE**: Web APIs, and some of the silent ways of acquiring tokens (Windows Integrated Authentication and username password) don't require a redirect URI.

### I've deployed my web application and when I test the deployed app, I get a reply url mismatch message

When you deploy your web application, you need to add redirect URIs for all the locations where you deploy it. See [Register a web app app using Azure portal](https://docs.microsoft.com/azure/active-directory/develop/scenario-web-app-sign-user-app-registration?tabs=aspnetcore#register-an-app-using-azure-portal).

### I can't register enough reply URLs

You're an ISV and have one or several redirect URIs per your customers. You want to migrate from ADAL/Azure AD v1.0 to MSAL/the Microsoft identity platform and you hit the [maximum number of redirect URIs](https://docs.microsoft.com/azure/active-directory/develop/reply-url#maximum-number-of-redirect-uris). To resolve this, [add redirect URIs to service principals](https://docs.microsoft.com/azure/active-directory/develop/reply-url#add-redirect-uris-to-service-principals) corresponding to each of your customers.

## **Recommended Documents**

* [Authentication flows and application scenarios](https://docs.microsoft.com/azure/active-directory/develop/authentication-flows-app-scenarios). In this article, you'll find useful information about the redirect URIs in the **App registration** page for each scenario.
* [Redirect URI/reply URL restrictions and limitations](https://docs.microsoft.com/azure/active-directory/develop/reply-url)
