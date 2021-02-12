<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-700016"
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

**Error Code:** 700016

**Message:** Application with identifier '{appIdentifier}' was not found in the directory '{tenantName}'. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You may have sent your authentication request to the wrong tenant.
<!--/issueDescription-->

**Action:** The application wasn't found in the directory/tenant. This can happen if the application has not been installed by the administrator of the tenant or consented to by any user in the tenant. You might have misconfigured the identifier value for the application or sent your authentication request to the wrong tenant.


