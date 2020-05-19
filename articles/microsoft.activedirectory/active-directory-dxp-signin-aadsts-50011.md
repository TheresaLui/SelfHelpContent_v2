<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-50011"
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

**Error Code:** 50011

**Message:** The reply URL specified in the request does not match the reply URLs configured for the application: '{identifier}'. {detail}
<!--/issueDescription-->

**Action:** The user's sign in failed since the application's reply URL value is misconfigured. To resolve this problem check documentation for the application or consult with the application administrators and enter the correct reply URL in the Azure AD application configuration view.<br><br>You can refer to the following links for the steps to resolve the issue.

<ul><li>You can view and manage the application configuration from <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps/menuId/'>Enterprise Applications</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/develop/reply-url'>Redirect URI/reply URL restrictions and limitations</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/manage-apps/application-sign-in-problem-federated-sso-non-gallery#the-reply-address-does-not-match-the-reply-addresses-configured-for-the-application'>Troubleshooting Guide</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/develop/app-registration-portal-training-guide#platformsauthentication-reply-urlsredirect-uris'>The new Azure portal app registration experience - Reply URLs/redirect URIs</a></li></ul>
