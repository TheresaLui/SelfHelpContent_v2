<properties
    pageTitle="SignIn Issues due to CA/MFA"
    description="Troubleshoot for CA/MFA related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-mfa-proofup-other-location"
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
Based on the information you provided the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName--> but the user sign-in was interrupted for required setup of Multi-Factor Authentication (MFA) but the client is not signing in from a trusted location for MFA to be setup from.
<!--/issueDescription-->

This can happen when the user is required to set up MFA for the first time, or when an admin has set their account to require a new proofup for some reason. 

The MFA setup cannot be done from the network location the client tried to sign-in from. The actions to resolve this are to have the user connect to a different or trusted network. For example, try again after connecting to a corporate network via VPN. 

Once connected to a trustworthy network the interrupt can be avoided by having the user finish the MFA setup (also known as "proofup").  This means the user would simply configure and verify the additional authentication methods for MFA. For example, if texting is the method the user would have to get the code on their phone and then enter it into the setup page. 

After proofup is done the user will be able to sign-in for the application they were trying to use. 

More information about the sign-in attempt is below. 

## **Sign-in Details**
<!--$signinDetails-->[signinDetails]<!--/$signinDetails-->

## **Authentication Details**
<!--$authReqDetails-->[authReqDetails]<!--/$authReqDetails-->

## **Recommended Documents**

* [What is the Additional verification page?](https://docs.microsoft.com/azure/active-directory/user-help/multi-factor-authentication-end-user-first-time )