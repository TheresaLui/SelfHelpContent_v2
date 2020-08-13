<properties
  pageTitle="Problems with my application"
  description="Solutions to known problems for my apps and info on ADAL deprecation"
  service="microsoft.aad"
  resource="Microsoft_AAD_IAM"
  authors="marwaIDCxP"
  ms.author="marwa"
  selfHelpType="generic"
  supportTopicIds="32570261"
  productPesIds="16575"
  cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
 	articleId="5c2cb674-d2dd-4874-87ac-a18593340dbe"
	ownershipId="AzureIdentity_AppDevelopmentAndRegistration"
/>

# Problems developing my application

## **Recommended Steps**

Below you will find help and links for the most common problems when building Azure Active Directory apps.  We highly recommend you check Stackoverflow for [issues building Azure Active Directory apps](https://stackoverflow.com/questions/tagged/azure-active-directory), the answer to your question may already be available. If you can't find an answer to your question, post a [question on StackOverflow with the tag `azure-active-directory`](https://stackoverflow.com/questions/ask).

## **Recommended Documents**

* **[I am seeing trouble signing in to application(s) using Chrome browser only](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications)**
* [I don't know how to change the token lifetime defaults for my application](https://docs.microsoft.com/azure/active-directory/application-dev-registration-config-change-token-lifetime-how-to/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I am confused about how application consent works](https://docs.microsoft.com/azure/active-directory/application-dev-consent-framework/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I don't know how to grant permissions to my application](https://docs.microsoft.com/azure/active-directory/application-dev-registration-config-grant-permissions-how-to/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I don't understand the difference between delegated and application permissions](https://docs.microsoft.com/azure/active-directory/application-dev-delegated-and-app-perms/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)

# End of support for Azure Active Directory Authentication Library (ADAL)

Starting June 30th, 2020, we will no longer add any new features to ADAL. We will continue to provide technical support and security updates but will no longer provide feature updates.

Starting June 30th, 2022, we will end support for ADAL and will no longer provide technical support or security updates. Apps using ADAL on existing OS versions will continue to work after this time but will not get any technical support or security updates.

We recommend updating to the Microsoft Authentication Library (MSAL), which has the latest features and security updates. [Learn more.](https://docs.microsoft.com/azure/active-directory/develop/v2-overview)

If you're using Microsoft apps, know that Microsoft is in the process of migrating its applications to MSAL by the end-of-support deadline, ensuring they'll benefit from MSAL's ongoing security and feature improvements.

## **Recommended Steps**

1. [Read the ADAL FAQ.](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq)

1. [Learn about the end of support timelines from the blog post here.](https://techcommunity.microsoft.com/t5/azure-active-directory-identity/update-your-applications-to-use-microsoft-authentication-library/ba-p/1257363)
 
1. [Learn about how to migrate apps on a per-platform basis.](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq)

1. If you need help understanding which of your apps use ADAL, we recommend you review all of your apps' source code, and if applicable, reach out to any ISVs or app providers. Microsoft support can also provide you with a list of all non-Microsoft ADAL apps in your tenant.

1. If you can't find an answer to your question, post a [question on StackOverflow with the tag `ADAL-deprecation`](https://stackoverflow.com/questions/ask).