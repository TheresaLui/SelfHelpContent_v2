<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="HuaTang"
    ms.author="hut"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-security-defaults"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Sign In Interrupted by Security Defaults

<!--issueDescription-->
Based on the information you provided, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into Office 365 (preview) and was interrupted by Security Defaults. Security Defaults enforce best practice security for your organization. These defaults require that you configure Multi-Factor Authentication (MFA) to prevent password sprays, replay attacks and phishing attempts from being successful.

Review what the client submitted for the sign-in and what happened during the authentication attempts:
<!--/issueDescription-->

## **Authentication details**
<!--$authDetails-->[authDetails]<!--/$authDetails-->

## **Sign-in details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Recommended Documents**

* [Security Defaults Enforced Settings](https://docs.microsoft.com/azure/active-directory/fundamentals/concept-fundamentals-security-defaults#policies-enforced)
