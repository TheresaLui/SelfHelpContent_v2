<properties
  pagetitle="Microsoft Graph authorization errors"
  service="microsoft.aad"
  resource="microsoft_aad_iam"
  ms.author="davidmu,riclewis"
  selfhelptype="Generic"
  supporttopicids="32689189,32596852"
  resourcetags=""
  productpesids="16952,16953,16954,16955,16956,16575"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="0ba3c716-5514-4e79-b7cc-9c0b3095dfe0"
  ownershipid="AzureIdentity_MSGraph" />

#### **IMPORTANT:** We're depricating Azure AD TLS 1.1 and 1.0 *soon*. Enable support for TLS 1.2 in your environment. For more details and dates, review [Enable support for TLS 1.2 in your environment for Azure AD TLS 1.1 and 1.0 deprecation](https://docs.microsoft.com/troubleshoot/azure/active-directory/enable-support-tls-environment)

# Microsoft Graph authorization errors

Authorization errors can be a result of several different issues, most of which generate a 401 or 403 error. For example, the following can all lead to authorization errors:

* Incorrect [access token acquisition flows](https://docs.microsoft.com/azure/active-directory/develop/active-directory-authentication-scenarios)
* Poorly configured [permission scopes](https://docs.microsoft.com/azure/active-directory/develop/active-directory-v2-scopes)
* Lack of [consent](https://docs.microsoft.com/azure/active-directory/develop/active-directory-devhowto-multi-tenant-overview#understanding-user-and-admin-consent)

## **Recommended Steps**

To resolve common authorization errors, try the steps provided below that most closely matches the error you are receiving. More than one may apply. You can also check the answers already available in Stack Overflow for [401 errors](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+401+isanswered%3Ayes+views%3A50) and [403 errors](https://stackoverflow.com/search?q=%5Bmicrosoft-graph%5D+403+isanswered%3Ayes+views%3A50). If you can't find a solution to your problem, [ask a new question on Stack Overflow](https://stackoverflow.com/questions/ask) and tag with *microsoft-graph*.

**401 Unauthorized error: Is your token valid?** <br>

Make sure that your application is presenting a valid access token to Microsoft Graph as part of the request. This error often means that the access token may be missing in the HTTP authenticate request header or that the token is invalid or has expired. We strongly recommend that you use the [Microsoft Authentication Library (MSAL)](https://docs.microsoft.com/azure/active-directory/develop/msal-overview) for access token acquisition. Additionally this error may occur if you try to use a delegated access token granted to a personal Microsoft account to access an API that only supports work or school accounts (organizational accounts). 

**403 Forbidden error: Have you chosen the right set of permissions?**<br>

Check that you have requested the correct set of permissions based on the Microsoft Graph APIs your app calls. Recommended least privileged permissions are provided in all the Microsoft Graph API reference method topics. Additionally, those permissions must be granted to the application by a user or an administrator. Granting permissions normally happens through a consent page or by granting permissions using the Azure Portal application registration blade. From the **Settings** blade for the application, click **Required Permissions**, and then click **Grant Permissions**. <br>

* [Microsoft Graph permissions](https://docs.microsoft.com/graph/permissions-reference) <br>
* [Understanding Azure AD permissions and consent](https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent) <br>

**403 Forbidden error: Did your app acquire a token to match chosen permissions?** <br>

Make sure that the type of permissions requested or granted matches the type of access token that your app acquires. You might be requesting and granting application permissions but using delegated interactive code flow tokens instead of client credential flow tokens, or requesting and granting delegated permissions but using client credential flow tokens instead of delegated code flow tokens.

* [Get access on behalf of users and delegated permissions](https://docs.microsoft.com/graph/auth_v2_user) 
* [Azure AD v2.0 - OAuth 2.0 authorization code flow](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-auth-code-flow)
* [Get access without a user (daemon service) and application permissions](https://docs.microsoft.com/graph/auth_v2_service)
* [Azure AD v2.0 - OAuth 2.0 client credentials flow](https://docs.microsoft.com/azure/active-directory/develop/v2-oauth2-client-creds-grant-flow)

**403 Forbidden error: Resetting password** <br>

Currently, there are no application permission daemon service-to-service permissions that allow resetting user passwords. These APIs are only supported using the interactive delegated code flows with a signed-in administrator.

* [Microsoft Graph permissions](https://docs.microsoft.com/graph/permissions-reference) <br>

**403 Forbidden: Does the user have access and are they licensed?** <br>

For delegated code flows, Microsoft Graph evaluates if the request is allowed based on the permissions granted to the app and the permissions that the signed-in user has. Generally, this error indicates that the user is not privileged enough to perform the request **or** the user is not licensed for the data being accessed. Only users with the required permissions or licenses can make the request successfully.

**403 Forbidden: Did you select the correct resource API?** <br>

API services like Microsoft Graph check that the *aud* claim (audience) in the received access token matches the value it expects for itself, and if not, it results in a 403 Forbidden error. A common mistake resulting in this error is trying to use a token acquired for Azure AD Graph APIs, Outlook APIs, or SharePoint/OneDrive APIs to call Microsoft Graph (or vice versa). Ensure that the resource (or scope) your app is acquiring a token for matches the API that the app is calling.

**400 Bad Request or 403 Forbidden: Does the user comply with their organization's conditional access (CA) policies?**<br>

Based on an organization's CA policies, a user accessing Microsoft Graph resources via your app may be challenged for additional information that is not present in the access token your app originally acquired. In this case, your app receives a 400 with an *interaction_required* error during access token acquisition or a 403 with *insufficient_claims* error when calling Microsoft Graph. In both cases, the error response contains additional information that can be presented to the authorize endpoint to challenge the user for additional information (like multi-factor authentication or device enrollment).

* [Handling conditional access challenges using MSAL](https://docs.microsoft.com/azure/active-directory/develop/msal-handling-exceptions#conditional-access-and-claims-challenges)
* [Developer guidance for Azure Active Directory conditional access](https://docs.microsoft.com/azure/active-directory/develop/conditional-access-dev-guide)


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
