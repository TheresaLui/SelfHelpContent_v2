<properties
  pagetitle="Problems developing my application"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="marwa,riclewis"
  selfhelptype="Generic"
  supporttopicids="32570261"
  resourcetags=""
  productpesids="16575"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="5c2cb674-d2dd-4874-87ac-a18593340dbe"
  ownershipid="AzureIdentity_AppDevelopmentAndRegistration" />
# Problems developing my application

Below you will find help and links for the most common problems when building Azure Active Directory apps.  We highly recommend you check Stackoverflow for [issues building Azure Active Directory apps](https://stackoverflow.com/questions/tagged/azure-active-directory), the answer to your question may already be available. If you can't find an answer to your question, post a [question on StackOverflow with the tag `azure-active-directory`](https://stackoverflow.com/questions/ask).

## **Recommended Documents**

* **[I am seeing trouble signing in to application(s) using Chrome browser only](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications)**
* [I don't know how to change the token lifetime defaults for my application](https://docs.microsoft.com/azure/active-directory/application-dev-registration-config-change-token-lifetime-how-to/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I am confused about how application consent works](https://docs.microsoft.com/azure/active-directory/application-dev-consent-framework/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I don't know how to grant permissions to my application](https://docs.microsoft.com/azure/active-directory/application-dev-registration-config-grant-permissions-how-to/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)
* [I don't understand the difference between delegated and application permissions](https://docs.microsoft.com/azure/active-directory/application-dev-delegated-and-app-perms/?WT.mc_id=UI_AAD_Registered_Apps_Support_L2_Overview)

## End of support for Azure Active Directory Authentication Library (ADAL) and Azure AD Graph API (AAD Graph)

**Starting June  30th, 2020**, we will no longer add any new features to ADAL and Azure AD Graph. We will continue to provide technical support and security updates but will no longer provide feature updates.

**Starting June  30th, 2022**, we will end support for ADAL and Azure AD Graph and will no longer provide technical support or security updates.

Apps using ADAL on existing OS versions will continue to work after this time but will not *get any  technical support or security updates.*

Apps using Azure AD Graph after this time may no longer receive responses from the Azure AD Graph endpoint. 

## **Recommended Steps**

### ADAL Migration
We recommend updating to the [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/v2-overview), which has the latest features and security updates. 

If you're using Microsoft apps, know that Microsoft is in the process of migrating its applications to MSAL by the end-of-support deadline, ensuring they'll benefit from MSAL's ongoing security and feature improvements.

1. [Read the ADAL FAQ](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq)
2. [Learn about how to migrate apps on a per-platform basis](https://docs.microsoft.com/azure/active-directory/develop/msal-migration#frequently-asked-questions-faq)
3. If you need help understanding which of your apps use ADAL, we recommend you review all of your apps' source code, and if applicable, reach out to any ISVs or app providers. Microsoft support can also provide you with a list of all non-Microsoft ADAL apps in your tenant.
4. If you can't find an answer to your question, post a [question on StackOverflow with the tag `ADAL-deprecation`](https://stackoverflow.com/questions/ask)


### AAD Graph Migration
For applications  that are using Azure AD Graph, follow our guidance to [migrate Azure AD Graph apps to Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-overview?view=graph-rest-1.0).

1. [Our migration checklist provides a getting started point.](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist)
2. Your Azure app registration portal shows which applications are using AAD Graph.  We recommend you review all of your apps' source code, and if applicable, reach out to any ISVs or app providers. Microsoft support can also provide you with a list of all AAD Graph usage in your tenant.
3. If you cannot find an answer to your question, post a [question on StackOverflow with the tag `azureadgraph-deprecation`](https://stackoverflow.com/questions/tagged/azureadgraph-deprecation)