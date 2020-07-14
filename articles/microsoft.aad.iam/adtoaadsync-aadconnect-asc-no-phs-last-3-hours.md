<properties
    pageTitle="AAD Connect server(s) did not sync passwords in the last 3 hours"
    description="No password sync in last 3 hours"
    infoBubbleText="No password sync in last 3 hours. See details on the right"
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="jecheria"
    ms.author="jecheria"
    displayOrder="1"
    articleId="ADtoAADSync_AADConnect_ASC_No_PasswordHashSynchronization_3Hours"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>

# AAD Connect server(s) did not sync passwords in the last 3 hours
<!--issueDescription-->
We detected that there has not been any password hash sync activity received for your tenant in the past 3 hours. This indicates that there is an issue with your on premises password synchronization feature.
<!--/issueDescription-->

## **Recommended Steps**

* [Troubleshoot password hash synchronization with Azure AD Connect sync](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-troubleshoot-password-hash-synchronization)