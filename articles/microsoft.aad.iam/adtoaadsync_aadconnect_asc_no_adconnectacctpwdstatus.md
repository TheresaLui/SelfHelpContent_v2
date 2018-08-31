<properties
	pageTitle="ADtoAADSync_AADConnect_ASC_No_ADConnectAcctPwdStatus"
	description="The AD DS account password has been changed but it has not been updated on the Synchronization Service AD Connector"
	infoBubbleText="The AD DS account password has been changed but it has not been updated on the Synchronization Service AD Connector. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_No_ADConnectAcctPwdStatus"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>
# The AD DS account password has been changed but it has not been updated on the Synchronization Service AD Connector
<!--issueDescription-->
## The AD DS account password has been changed but it has not been updated on the Synchronization Service AD Connector
We have detected that the Active Directory account password on your Azure AD Connect server has been changed but it has not been updated on the Synchronization Service AD  Connector. As a consequence, the Synchronization Service will no longer be able to import/export changes to on-premises.

You may see the following:

- The import/export step for the AD connector fails with "no-start-credentials" error.
- Under Windows Event Viewer, the application event log contains an error with Event ID 6000 and message “The management agent “contoso.com” failed to run because the credentials were invalid.”
<!--/issueDescription-->
## **Recommended steps**

To resolve the issue, update the Active Directory user account using the steps as show in [this article](https://docs.microsoft.com/en-us/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-connectors#changing-the-ad-ds-account-password)

