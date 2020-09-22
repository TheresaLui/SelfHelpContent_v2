<properties
    pageTitle="Azure Active Directory (Azure AD) didn't register a synchronization attempt in the last 24 hours"
    description="No Synchronization registered within the last 24 hours"
    infoBubbleText="No Synchronization registered within the last 24 hours. See details on the right"
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="jecheria"
    ms.author="jecheria"
    displayOrder="1"
    articleId="ADtoAADSync_AADConnect_ASC_No_Synchronization_24Hours"
    diagnosticScenario=""
    selfHelpType="Diagnostics"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>

# Azure Active Directory (Azure AD) didn't register a synchronization attempt in the last 24 hours
<!--issueDescription-->
We detected that Azure Active Directory Sync (Azure AD Sync) didn't synchronize in the past 24 hours. By default, directory synchronization runs every three hours.
<!--/issueDescription-->

## **Recommended Steps**

This issue may occur if one or more of the following conditions are true:

* The work or school account that was used in the configuration wizard to set up directory synchronization has one of the following problems:

  * The account was deleted
  * The account was disabled
  * The account password expired

* The logon account for one or more directory synchronization services has one of the following problems:

  * The account was deleted
  * The account was disabled
  * The account password expired

* The admin account that's used for directory synchronization was changed
* You have network connection issues

To resolve this issue, review the [Directory synchronization to Azure Active Directory stops or you're warned that sync hasn't registered in more than a day](https://support.microsoft.com/help/2882421/directory-synchronization-to-azure-active-directory-stops-or-you-re-wa) article.