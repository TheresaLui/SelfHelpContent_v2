<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-classic-policy-other"
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
Based on the information you provided the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName--> but was interrupted by a Classic Conditional Access policy.
<!--/issueDescription-->

Classic policies are older policies which were created in the Azure classic portal, the Intune classic portal, or the Intune App Protection portal. Classic policies have limited capabilities and reporting. They can also be difficult to troubleshoot.  

We recommend that you migrate all Classic policies to new Conditional Access policies.  

* View the Classic policies in your tenant [here](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/ClassicPolicies)
* Learn how to migration the Classic policies by following the steps in this [article](https://docs.microsoft.com/azure/active-directory/conditional-access/policy-migration) 

More information about the sign-in attempt is below. 

## **Sign-in Details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Authentication Details**
<!--$authReqDetails-->[authReqDetails]<!--/$authReqDetails-->
