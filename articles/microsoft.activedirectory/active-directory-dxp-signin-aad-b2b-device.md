<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="HuaTang"
    ms.author="hut"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-b2b-device"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# B2B Sign-in Interrupted by Conditional Access

<!--issueDescription-->
Based on the information you provided, the B2B user <!--$userName-->[userName]<!--/$userName--> was trying to sign into Office 365 (preview) and sign in was interrupted by one or more Conditional Access policies that required the user's device or client application to be managed your organization.

Since the user is from a different organization, the device would be managed by the other organization, if at all. 

The following policies gave the interruption:
<!--/issueDescription-->

<!--$policyNames-->[policyNames]<!--/$policyNames-->

Additional the client submitted for the sign-in attempt and policy in question:

<!--$devicesDetails-->[devicesDetails]<!--/$devicesDetails-->

[Edit Conditional Access Policies](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies)

## **Recommended Documents**

* [B2B Sign-in and Device-based Conditional Access](https://docs.microsoft.com/azure/active-directory/external-identities/conditional-access#device-based-conditional-access)
* [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access)
