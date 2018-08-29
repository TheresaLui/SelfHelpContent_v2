<properties
	pageTitle="Export deletion threshold has been reached"
	description="Export deletion threshold has been reached"
	infoBubbleText="Found that export deletion threshold has been reached. See details on the right"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="neliceat"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_Export_Deletion_Threshold_Alert_Being_Generated"
	diagnosticScenario=""
	selfHelpType="diagnostics"
	supportTopicIds=""
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>
<!--issueDescription-->
# Export deletion threshold has been reached
When installing Azure AD Connect, "*prevent accidental deletes*" is enabled by default and configured to not allow an export with more than 500 deletes. This feature is designed to protect you from accidental configuration changes and changes to your on-premises directory that would affect many users and other objects.

What is *prevent accidental deletes*? Common scenarios when you see many deletes in Azure AD Connect include:

- Changes to filtering where an entire OU or domain is unselected.
- All objects in an OU are deleted.
- An OU is renamed so all objects in it are considered to be out of scope for synchronization.
<!--/issueDescription-->

## **Recommended steps**

Depending on your specific issue, there may be one of two situations:

- The deletes were accidental and you did not want these deletions to take place. In that case, you should undo the accidental changes that triggered the deletions. AADConnect will resume its normal operation after the accidental changes have been mitigated.
- You intended to delete more objects than the threshold allows. In this case you can disable the deletion threshold by issuing the following PowerShell cmdlet:

`Import-Module ADSync`

`Disable-ADSyncExportDeletionThreshold`

After issuing this cmdlet the pending objects will be deleted in Azure AD. 

Note: You should re-enable the deletion threshold after the objects are deleted from Azure AD, using this cmdlet:

`Enable-ADSyncExportDeletionThreshold`


## **Recommended documents**
* [AADConnect sync feature - Prevent accidental deletes](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-feature-prevent-accidental-deletes)<br>
