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
Based on the information you provided, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName-->, but MFA authentication was required.
<!--/issueDescription-->

If the prompt for MFA was unexpected, review the details below to see why it happened and what may be done to resolve any issues.

MFA was required due to:
<!--$possibleFixes-->[possibleFixes]<!--/$possibleFixes--> 

Review the following authentication details to get insight into what MFA methods were attempted and whether they succeeded or not.
For additional steps on how to troubleshoot, refer to the guidance in the Recommended Documents section.

## **Authentication Details**
<!--$authReqDetails-->[authReqDetails]<!--/$authReqDetails-->

## **Sign-in Details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Recommended Documents**

* [Common problems with two-factor verification and your work or school account](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-troubleshoot)
* [User help documentation](https://docs.microsoft.com/azure/active-directory/user-help/)
