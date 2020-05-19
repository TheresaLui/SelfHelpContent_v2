<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-650056"
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

**Error Code:** 650056

**Message:** Misconfigured application. This could be due to one of the following: The client has not listed any permissions for '{name}' in the requested permissions in the client's application registration. Or, The admin has not consented in the tenant. Or, Check the application identifier in the request to ensure it matches the configured client application identifier. Please contact your admin to fix the configuration or consent on behalf of the tenant. Client app ID: {id}.
<!--/issueDescription-->

**Action:** This could be due to one of the following reasons.<br>1.The application may not have the permissions needed to perform what the app requested.<br>2.The user or admin does not have consent for the app to run.<br>3.The issue could be that the client supplied the wrong application identifier in the sign in request.<br>4.The certificate in the request may be invalid.<br><br>You can refer to the following link for the steps to resolve the issue.

<ul><li>You can view and manage the application configuration from <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/StartboardApplicationsMenuBlade/AllApps/menuId/'>Enterprise Applications</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/manage-apps/configure-user-consent'>Configure how end-users consent to applications</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/develop/v2-permissions-and-consent'>Permissions and consent in the Microsoft identity platform endpoint</a></li></ul>
