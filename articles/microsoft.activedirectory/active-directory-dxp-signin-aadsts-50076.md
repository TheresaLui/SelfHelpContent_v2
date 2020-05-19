<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-50076"
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

**Error Code:** 50076

**Message:** Due to a configuration change made by your administrator, or because you moved to a new location, you must use multi-factor authentication to access '{resource}'.
<!--/issueDescription-->

**Action:** The user was required to provide MFA for the sign in. This may have occurred due to the following reasons:<br>1. A conditional access policy that requires MFA based on sign in factors like client type, geographic location, group membership, or application<br>2.The MFA requirement is enabled at user level or<br>3. The application the user was signing into may have requested MFA.<br><br>To find out more information about why the user was prompted for MFA review the Azure AD sign in event Authentication Details and Conditional Access tabs.<br><br>You can refer to the following link for the steps to resolve the issue.

<ul><li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/authentication/howto-mfa-userstates'>Enable per-user Azure Multi-Factor Authentication to secure sign-in events</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/azuread-dev/conditional-access-dev-guide'>Developer guidance for Azure Active Directory Conditional Access</a></li></ul>
