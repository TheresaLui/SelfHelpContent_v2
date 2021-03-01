<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="HuaTang"
    ms.author="hut"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-legacy-auth"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Sign In Failed due to Legacy Authentication

<!--issueDescription-->
Based on the information you provided, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into Exchange Online and was not allowed to sign-in since the client attempted to authenticate using a legacy authentication protocol. 

Preventing legacy authentication sign-in is recommended as a best practice for security. Legacy authentication protocols like POP, SMTP, IMAP, and MAPI cannot enforce Multi-Factor Authentication (MFA) which makes them preferred entry points for adversaries to attack your organization.

The policy or policies that prevented the sign-in:
<!--/issueDescription-->

<!--$policyNames-->[policyNames]<!--/$policyNames-->

Review the application and client information in the following Sign-in Details for more information about this sign-in attempt. 

Note: Exchange Online is removing support for Basic Authentication (another name for legacy authentication). More information is available in the links below.

## **Recommended Documents**

* [Exchange Online deprecating Basic Authentication](https://docs.microsoft.com/lifecycle/announcements/exchange-online-basic-auth-deprecated)
* [How to: Block legacy authentication to Azure AD with Conditional Access](https://docs.microsoft.com/azure/active-directory/conditional-access/block-legacy-authentication)

## **Sign-in details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->
