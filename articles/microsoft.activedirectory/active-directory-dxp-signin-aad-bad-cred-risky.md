<properties
    pageTitle="SignIn Issues due to Incorrect Credentials"
    description="Troubleshoot for Incorrect Credentials related signin issues"
    infoBubbleText="See details on the right"
    service="microsoft.activedirectory"
    resource=""
    authors="vritiJain"
    ms.author="vrjai"
    displayOrder="1"
    articleId="active-directory-dxp-signin-aad-bad-cred-risky"
    diagnosticScenario="EnterpriseApps"
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="AzureIdentity_IdentityDiagnostics"
/>

# Azure AD Smart Lockout: Blocked Sign-in of Risky User

<!--issueDescription-->
In this sign-in attempt, the user <!--$userName-->[userName]<!--/$userName--> was trying to sign into <!--$appName-->[appName]<!--/$appName--> but the user had attempted sign-in with incorrect credentials too many times. In addition to this behavior, Identity Protection has identified that this user is a risky user. Azure AD continually evaluates user risk based on various signals and machine learning.
<!--/issueDescription-->

<!--$stepResultDetail-->[stepResultDetail]<!--/$stepResultDetail-->

Microsoft recommends that this user and their activity be investigated immediately. More information on how to investigate risk is available under Helpful Content below.

## **Risky User Details**
<!--$riskContent-->[riskContent]<!--/$riskContent-->

[Risky users report](https://portal.azure.com/#blade/Microsoft_AAD_IAM/SecurityMenuBlade/RiskyUsers)

## **Recommended Documents**

* [How To Investigate risk](https://docs.microsoft.com/azure/active-directory/identity-protection/howto-identity-protection-investigate-risk)