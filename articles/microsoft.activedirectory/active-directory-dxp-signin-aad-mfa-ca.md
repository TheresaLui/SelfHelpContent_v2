<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-mfa-ca"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Multi-Factor Authentication(MFA) needed for Sign-in

<!--issueDescription-->
Based on the information you provided, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName-->, but MFA authentication was required by the Conditional Access policy or policies below:
<!--/issueDescription-->

<!--$policyNames-->[policyNames]<!--/$policyNames-->

If the prompt for MFA was unexpected, review the following details to see why it happened and what may be done to resolve any issues.

Included in the information are the application conditions from the Conditional Access policy or policies that applied and the Sign-in event details that the client submitted for the sign-in attempt that matched the policy conditions.

<!--$policyConditions-->[policyConditions]<!--/$policyConditions-->
[Edit Conditional Access Policies](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies)

## **Authentication Details**
<!--$authReqDetails-->[authReqDetails]<!--/$authReqDetails-->

## **Recommended Documents**

* [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access)
* [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/what-if-tool)
