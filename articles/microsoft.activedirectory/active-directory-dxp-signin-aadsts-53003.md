<properties
    pageTitle="SignIn Issues"
    description="Common signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aadsts-53003"
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

**Error Code:** 53003

**Message:** Access has been blocked by one or more Conditional Access policies with access controls configured to block.
<!--/issueDescription-->

**Action:** The user sign in was blocked by a conditional access policy. If this block was unexpected, review the conditional access policy configuration which applied to the sign in attempt. The conditional access policy can be found in the Azure AD sign in event entry in the Conditional Access tab. Simply click on the policy or policies to view the settings or change the settings as needed. If the block was an expected result for the sign in attempt more details can be found for review in the sign in event as well.<br><br>You can refer to the following link for the steps to resolve the issue.

<ul><li>You can view additional information in the <a href='https://portal.azure.com/#blade/Microsoft_AAD_IAM/SignInEventsV3Blade/{key}/{value}/'>Sign-in Logs</a></li><li> <a href='https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access'>Troubleshooting sign-in problems with Conditional Access</a></li></ul>
