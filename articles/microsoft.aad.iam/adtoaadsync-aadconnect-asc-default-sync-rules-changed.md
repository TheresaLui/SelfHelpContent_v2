<properties
    pageTitle="Default synchronization rules have been changed"
    description="Default synchronization rules have been changed"
    infoBubbleText="Found that some default synchronization rules have been modified. See details on the right"
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="neliceat"
    ms.author="neliceat"
    displayOrder="1"
    articleId="AADtoADSync_AADConnect_ASC_Default_Sync_Rules_Changed"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds="32404459"
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>

# Default synchronization rules have been changed
<!--issueDescription-->
Synchronization rules are a critical component in the Azure AD Connect (AADConnect) configuration, and when AADConnect is first installed it comes with several default synchronization rules. One or more default synchronization rules in your Azure AD Connect installation have been modified. We do not support changes made to the default synchronization rules.
<!--/issueDescription-->

## **Recommended Steps**

1. If you need to change the way a synchronization rule behaves, you should instead create a clone of the default synchronization rule and modify that cloned copy. This article provides details about how to modify synchronization rules in a supported manner: [Best practices changing default configuration - Changes to synchronization rules](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-best-practices-changing-default-configuration#changes-to-synchronization-rules)
2. Synchronization rules are implemented through a declarative provisioning  model, and you can read more about this model in this article: [Understanding declarative provisioning](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-understanding-declarative-provisioning)
3. To recover from this issue, you must clone the modified rule. By doing so, their changes will not be overwritten when the AADConnect deployment is upgraded to a new version. This document describes in detail how to do this: [Best practices changing default configuration - Change an out-of-box rule](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-best-practices-changing-default-configuration#change-an-out-of-box-rule) <br>


## **Recommended Documents**

* [Learn more about the Default Synchronization Rules in Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-understanding-default-configuration#synchronization-rule)<br>