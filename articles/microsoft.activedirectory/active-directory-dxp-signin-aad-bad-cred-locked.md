<properties
    pageTitle="SignIn Issues due to Incorrect Credentials"
    description="Troubleshoot for Incorrect Credentials related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-bad-cred-locked"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Azure AD Smart Lockout: Blocked Sign-in Attempt

<!--issueDescription-->
An attempt was made to sign in as <!--$userName-->[userName]<!--/$userName--> to <!--$appName-->[appName]<!--/$appName--> but the user had attempted sign-in with incorrect credentials too many times.
<!--/issueDescription-->

This user has had <!--$badAttempts-->[badAttempts]<!--/$badAttempts--> similar attempts locked out by Smart Lockout over the past 48 hours. Sign-in was blocked because it came from an IP address with malicious activity.

Smart lockout helps lock out bad actors that try to guess your users' passwords or use brute-force methods to get in. Smart lockout can recognize sign-ins that come from valid users and treat them differently than ones of attackers and other unknown sources. Attackers get locked out, while your users continue to access their accounts and be productive.

## **Blocked attempts for <!--$userName-->[userName]<!--/$userName--> (past 48 hours)**
<!--$attemptContent-->[attemptContent]<!--/$attemptContent-->

## **Sign-in details for this attempt**
<!--$signinContent-->[signinContent]<!--/$signinContent-->

## **Recommended Documents**

* [Protect user accounts from attacks with Azure Active Directory smart lockout](https://docs.microsoft.com/azure/active-directory/authentication/howto-password-smart-lockout)
