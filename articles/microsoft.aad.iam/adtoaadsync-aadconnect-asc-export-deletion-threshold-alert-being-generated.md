<properties
    pageTitle="Export deletion threshold has been reached"
    description="Export deletion threshold has been reached"
    infoBubbleText="Found that export deletion threshold has been reached. See details on the right"
    service="microsoft.aad.iam"
    resource="aadconnect"
    authors="neliceat"
    ms.author="neliceat"
    displayOrder="1"
    articleId="ADtoAADSync_AADConnect_ASC_Export_Deletion_Threshold_Alert_Being_Generated"
    diagnosticScenario=""
    selfHelpType="diagnostics"
    supportTopicIds=""
    resourceTags=""
    productPesIds="14785"
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
    ownershipId="Identity_AuthReach_HybridAuth_ADFS"
/>

# Export deletion threshold has been reached
<!--issueDescription-->
When installing Azure AD Connect, 'prevent accidental deletes' is enabled by default and configured to not allow an export with more than 500 deletes. This feature is designed to protect you from accidental configuration changes and changes to your on-premises directory that would affect many users and other objects.
<!--/issueDescription-->

## **Recommended Steps**

Depending on your specific issue, there may be one of two scenarios:

- The deletes were accidental and you did not want these deletions to take place. In that case, you should undo the accidental changes that triggered the deletions. Azure AD Connect will resume its normal operation after the accidental changes have been mitigated.
- You intended to delete more objects than the threshold allows. In this case, you can disable the deletion threshold by issuing the following PowerShell cmdlets:

`Import-Module ADSync`

`Disable-ADSyncExportDeletionThreshold`

After issuing this cmdlet the pending objects will be deleted in Azure AD.

**NOTE**: You should re-enable the deletion threshold after the objects are deleted from Azure AD, using this cmdlet:

`Enable-ADSyncExportDeletionThreshold`

## **Recommended Documents**

* [AADConnect sync feature - Prevent accidental deletes](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-prevent-accidental-deletes)<br>