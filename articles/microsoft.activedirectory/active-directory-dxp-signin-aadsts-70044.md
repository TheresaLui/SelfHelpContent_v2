<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-70044"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# How Do I Resolve the User Sign-in Issues?

<!--issueDescription-->
Based on the information you provided we have identified following issue and recommend taking the action to resolve the issue.

**Error Code:** 70044

**Message:** The session has expired or is invalid due to sign-in frequency checks by conditional access.
<!--/issueDescription-->

**Recommended Steps:**
The user's sign in token has expired and the client needs to sign into the application again. This may be the result of normal token expiration or a session control policy in conditional access. To resolve this issue either have the user sign in again or change the session control configuration in the conditional access policy.<br><br>You can refer to the following links for the steps to resolve the issue.

You can view additional information in the [Sign-in Logs](https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value})<br> [Configure authentication session management with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime#user-sign-in-frequency)<br>
