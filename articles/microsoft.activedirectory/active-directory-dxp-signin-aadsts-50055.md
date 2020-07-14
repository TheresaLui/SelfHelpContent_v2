<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-50055"
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

**Error Code:** 50055

**Message:** The password is expired.
<!--/issueDescription-->

**Action:** Either the user's password has expired or the user's refresh tokens have been revoked. The user's password may need to be changed on premise if password hash synchronization is done. To determine if the user needs a new password, check the user at the source of authority (Azure AD for cloud user or AD on premise for hybrid).  In addition, check whether the user's refresh tokens have been revoked using Azure AD Powershell's Get-AzureADUser cmdlet and review the RefreshTokensValidFromDateTime value date.<br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li> <a href='https://docs.microsoft.com/azure/active-directory/fundamentals/active-directory-users-reset-password-azure-portal'>Reset a user's password using Azure Active Directory</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/devices/concept-primary-refresh-token'>What is a Primary Refresh Token?</a></li></ul>
