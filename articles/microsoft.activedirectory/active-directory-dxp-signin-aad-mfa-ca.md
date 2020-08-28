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
Based on the information you provided the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName--> but MFA authentication was required by the conditional access policy or policies below:
<!--/issueDescription-->

<!--$policyNames-->[policyNames]<!--/$policyNames-->

If the prompt for MFA was unexpected be sure to expand the 'Show more' selection below.

Included in the information are the application conditions from the conditional access policy or policies which applied and the Sign-in event details which the client submitted for the sign in attempt which matched the policy conditions.

<!--$policyConditions-->[policyConditions]<!--/$policyConditions-->
[Edit Conditional Access Policies](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies)

## **Authentication Details**
<!--$mfaDetails-->[mfaDetails]<!--/$mfaDetails-->

## **Recommended Documents**

* [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access)
* [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/what-if-tool)