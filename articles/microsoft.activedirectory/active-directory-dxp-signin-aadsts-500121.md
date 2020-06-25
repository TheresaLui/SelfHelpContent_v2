<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-500121"
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

**Error Code:** 500121

**Message:** Authentication failed during strong authentication request.

<!--/issueDescription-->

**Action:** An MFA request was sent to the user using one of the methods they had configured but we did not receive a response. This could be a problem with the default strong authentication method selected by the user, a problem with the mobile device, a potential problem with the user's mobile carrier, or the recipient did not respond in an expected amount of time.<br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot'>Common problems with two-factor verification and your work or school account</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/authentication/multi-factor-authentication-faq'>Frequently asked questions about Azure Multi-Factor Authentication</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/reports-monitoring/concept-sign-ins'>Sign-in activity reports in the Azure Active Directory portal</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/authentication/concept-authentication-methods'>What authentication and verification methods are available in Azure Active Directory?</a></li></ul>
