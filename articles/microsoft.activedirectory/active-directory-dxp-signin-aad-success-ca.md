<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-success-ca"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Sign In Blocked

<!--issueDescription-->
Based on the information you provided the user <!--$userName-->[userName]<!--/$userName--> signed into <!--$appName-->[appName]<!--/$appName-->. 
No Conditional Access policies interrupted or blocked the sign-in. 
<!--/issueDescription-->

If the sign-in should have been blocked, or had a Multi-Factor Authentication (MFA) interrupt, or had some other control which was not seen for this sign-in, be sure to review the sign-in event details submitted by the client below.  

If any Conditional Access policies applied to the sign-in but were successful they are listed below for review.  

If a Conditional Access policy is not listed below the policy conditions were not met, the policy is not enabled or the policy is in report-only mode.  

View all your policies [here](https://portal.azure.com/#blade/Microsoft_AAD_IAM/ConditionalAccessBlade/Policies).

## **Successful Policies**
<!--$policyConditions-->[policyConditions]<!--/$policyConditions-->

## **Sign-in Details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Authentication Details**
<!--$authReqDetails-->[authReqDetails]<!--/$authReqDetails-->

## **Recommended Documents**

* [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/what-if-tool)
* [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access)
