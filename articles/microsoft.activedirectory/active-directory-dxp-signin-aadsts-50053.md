<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-50053"
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

**Error Code:** 50053

**Message:** The account is locked, you've tried to sign in too many times with an incorrect user ID or password.
<!--/issueDescription-->

**Action:** The user, an application with old stored credentials of the user, or someone trying to sign in as the user, has attempted to sign in to the account using an incorrect password too many times. Review the user's sign ins in the Azure AD Sign-in events to determine the specific source of incorrect password.<br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-sign-ins'>Sign-in activity reports in the Azure Active Directory portal</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/authentication/howto-password-smart-lockout'>Azure Active Directory smart lockout</a></li></ul>
