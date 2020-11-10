<properties
  pagetitle="Microsoft Graph authentication token issues"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="davidmu,riclewis"
  selfhelptype="Generic"
  supporttopicids="32689192,32596860"
  resourcetags=""
  productpesids="16952,16575"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2e5a474e-839f-432d-8bf3-7ed39d7635c3"
  ownershipid="AzureIdentity_MSGraph" />
# Microsoft Graph authentication token issues

This topic deals with failures to acquire access tokens to call Microsoft Graph. These issues may also be related to any failure to grant consent to access Microsoft Graph, for your application.

## **Recommended Steps**

Check the answers already available in Stack Overflow for [Microsoft Graph and authentication](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+authentication+isanswered%3Ayes+views%3A50), or craft your own, more specific search query. If you can't find a solution to your problem, [ask a new question on Stack Overflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

We strongly recommend the use of the [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/msal-overview) to acquire access tokens to call Microsoft Graph.

Review [Authentication flows and application scenarios](https://docs.microsoft.com/azure/active-directory/develop/authentication-flows-app-scenarios#scenarios-and-supported-platforms-and-languages) to see which scenario your application falls under, and follow the token acquisition guidance, language/platform support, and samples for that scenario. This represents the most comprehensive list, but the two most common scenarios are also described below.

**How do I authenticate and get an access token to Microsoft Graph?**

To authorize your app, authenticate the user first. You do this by redirecting the user to the Azure Active Directory (Azure AD) authorization endpoint, along with your app information, to sign users in to their work or school account, or their personal Microsoft account. After the user signs in and consents to the permissions requested by your app (if the user has not done so already), your app receives an authorization code that can be redeemed for an OAuth2.0 access token. You might also have a cached refresh token that you can redeem for an OAuth access token.

* [Call Microsoft Graph on behalf of the signed-in user](https://developer.microsoft.com/graph/docs/concepts/auth_v2_user)

**How do I call Microsoft Graph from a daemon service where there is no user signed-in?**

For service or daemon apps, your application should implement the OAuth 2.0 Client Credentials Grant Flow. Instead of impersonating a user, the app uses its own credentials, client ID, and application key to authenticate when calling the Microsoft Graph.

* [Call Microsoft Graph in a service or daemon app](https://developer.microsoft.com/graph/docs/authorization/app_only) 

**How do I get more information about AADSTS error codes?**

For more information, see [Authentication and authorization error codes](https://docs.microsoft.com/azure/active-directory/develop/reference-aadsts-error-codes).

## **Recommended Documents**

* [I am seeing trouble signing in to application(s) using Chrome browser only](https://docs.microsoft.com/office365/troubleshoot/miscellaneous/chrome-behavior-affects-applications)


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