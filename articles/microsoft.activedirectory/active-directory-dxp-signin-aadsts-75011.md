<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-75011"
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

**Error Code:** 75011

**Message:** Authentication method '{usedMethod}' by which the user authenticated with the service doesn't match requested authentication method '{requestedMethod}'. Contact the {appName} application owner.
<!--/issueDescription-->

**Action:** Some applications require a specific authentication method however in this case the authentication method configured in the app on the Azure AD side wasn't what the app wanted. To resolve this problem review the application configuration in Azure AD and ensure that the app is configured correctly based on what the application side wants. This usually requires consulting application documentation or contacting the app side administrators. Resolving this problem may require consulting application documentation, checking the application service side config, or contacting application side administrators for help.


