<properties
  pagetitle="Issues that are related to Azure Active Directory Application Management"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="riclewis,runuguse"
  selfhelptype="Generic"
  supporttopicids="32570274"
  resourcetags=""
  productpesids="16575"
  cloudenvironments="public,fairfax,mooncake,usnat,ussec"
  articleid="eaf4bf4e-f901-4448-a298-d7f63f33ef56"
  ownershipid="AzureIdentity_AppDevelopmentAndRegistration" />
# Issues that are related to Azure Active Directory Application Management

## **Recommended Steps**

The following links will bring you to a content map which will help you to resolve some of the most common issues faced when managing **Enterprise Applications** in Azure Active Directory.

* [Issues that are related to Application Configuration](https://docs.microsoft.com/azure/active-directory/active-directory-application-config-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to Sign-in](https://docs.microsoft.com/azure/active-directory/active-directory-application-sign-in-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to Provisioning](https://docs.microsoft.com/azure/active-directory/active-directory-application-provisioning-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to Managing Access](https://docs.microsoft.com/azure/active-directory/active-directory-application-access-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to the Access Panel](https://docs.microsoft.com/azure/active-directory/active-directory-application-access-panel-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to the Application Proxy](https://docs.microsoft.com/azure/active-directory/active-directory-application-proxy-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)
* [Issues that are related to Conditional Access](https://docs.microsoft.com/azure/active-directory/active-directory-application-conditional-access-content-map/?WT.mc_id=UI_AAD_Enterprise_Apps_Support_L1_Overview)


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
4. If you can't find an answer to your question, post a [question on Microsoft Q&A with the tag `azure-ad-adal-deprecation`](https://docs.microsoft.com/answers/questions/ask.html)


### AAD Graph Migration
For applications  that are using Azure AD Graph, follow our guidance to [migrate Azure AD Graph apps to Microsoft Graph](https://docs.microsoft.com/graph/migrate-azure-ad-graph-overview?view=graph-rest-1.0).

1. [Our migration checklist provides a getting started point.](https://docs.microsoft.com/graph/migrate-azure-ad-graph-planning-checklist)
2. Your Azure app registration portal shows which applications are using AAD Graph.  We recommend you review all of your apps' source code, and if applicable, reach out to any ISVs or app providers. Microsoft support can also provide you with a list of all AAD Graph usage in your tenant.
3. If you cannot find an answer to your question, post a [question on Microsoft Q&A with the tag `microsoft-graph-*`](https://docs.microsoft.com/answers/search.html?type=question&q=microsoft-graph-*)