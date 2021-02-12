<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-50158"
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

**Error Code:** 50158

**Message:** External security challenge not satisfied.

<!--/issueDescription-->

**Action:** There is no administrative action required. The user is required to satisfy additional requirements before finishing authentication, and was redirected to an external platform to complete the requirement (such as terms of use, an external MFA provider, or a Conditional Access custom control). To determine if the attempt was successful please review the sign-in logs. This interrupt alone does not indicate a failure on your users part to sign in.

<li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li></ul>
