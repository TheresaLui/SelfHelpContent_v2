<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="HuaTang"
    ms.author="hut"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-risk-policy"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Sign In Interrupted by Risk Policy

<!--issueDescription-->
Based on the information you provided, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into Office 365 (preview) and was interrupted by Identity Protection risk policy. 

Review what the client submitted for the sign-in attempt and user risk information (if available):
<!--/issueDescription-->

## **Risky User Details**
<!--$riskyUserDetails-->[riskyUserDetails]<!--/$riskyUserDetails-->

[Risk Detections](https://portal.azure.com/#blade/Microsoft_AAD_IAM/IdentityProtectionMenuBlade/RiskDetections)

## **Sign-in details for this attempt**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Recommended Documents**

* [How To: Investigate risk](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk )
