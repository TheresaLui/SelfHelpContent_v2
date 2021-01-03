<properties
    pageTitle="Problem with external users and self-service sign up"
    description="Problem with external users and self-service sign up"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="jkdouglas"
    ms.author="jodougla"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32741680"
    resourceTags=""
    productPesIds="16578"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="active-directory-b2b-self-service-sign-up.md"
	ownershipId="AzureIdentity_B2C"
/>

# Problem with self-service sign up

**Announcement** 
* [Deprecation of WebView sign-in support from Google starting January 4, 2021](https://docs.microsoft.com/azure/active-directory/external-identities/google-federation#deprecation-of-webview-sign-in-support). Test whether your apps may be affected by following [Google’s guidance](https://developers.googleblog.com/2020/08/guidance-for-our-effort-to-block-less-secure-browser-and-apps.html) on testing compatibility
* Make sure you use the system webview or system browser when signing in your users with consumer Google accounts
           
## **Recommended Steps**

* To use self-service sign-up with your applications, you must first [enable self-service sign-up for your tenant](https://docs.microsoft.com/azure/active-directory/b2b/self-service-sign-up-user-flow#enable-self-service-sign-up-for-your-tenant)
* To enable an application to support self-service sign-up, you must [add it to your user flow](https://docs.microsoft.com/azure/active-directory/b2b/self-service-sign-up-user-flow#add-applications-to-the-self-service-sign-up-user-flow). The next time you go to the login page for that application, you'll see an option for ***No account? Create one!***. This starts the self-service sign-up process.

## **Recommended Documents**

* [Self-service sign-up documentation](https://docs.microsoft.com/azure/active-directory/b2b/self-service-sign-up-user-flow)
