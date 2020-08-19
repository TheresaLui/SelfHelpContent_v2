<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-mfa-other"
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
Based on the information you provided the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName--> but a MFA authentication was required.
<!--/issueDescription-->

MFA was required due to:
<!--$possibleFixes-->[possibleFixes]<!--/$possibleFixes--> 

If the prompt for MFA was unexpected be sure to expand the 'Show more' selection below.

Review the authentication details below to get insight into what MFA methods were attempted and whether they succeeded or not.
For additional steps on how to troubleshoot you can refer to the guidance in the Recommended Documents.

## **Authentication Details**
<!--$mfaDetails-->[mfaDetails]<!--/$mfaDetails-->

## **Sign-in Details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Recommended Documents**

* [Troubleshooting sign-in problems with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/troubleshoot-conditional-access)
* [Troubleshoot using the What If tool in Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/what-if-tool)