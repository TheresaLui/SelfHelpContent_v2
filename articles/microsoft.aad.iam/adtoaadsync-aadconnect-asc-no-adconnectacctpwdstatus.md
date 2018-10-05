<properties
	pageTitle="ADtoAADSync_AADConnect_ASC_No_ADDSConnectAcctPwdStatus"
	description="The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS connector"
	infoBubbleText="The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS Connector. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_No_ADDSConnectorAcctPwdStatus"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="14785"
	cloudEnvironments="public"
/>
# The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS connector
<!--issueDescription-->
## The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS connector
We have detected that the Active Directory (AD) account password on your Azure AD Connect server has been changed but it has not been updated on the synchronization service AD DS connector. As a consequence, the synchronization service will no longer be able to import/export changes to on-premises.

You may see the following:

- The import/export step for the AD DS connector fails with "no-start-credentials" error.
- Under Windows Event Viewer, the application event log contains an error with Event ID 6000 and message “The management agent 'contoso.com' failed to run because the credentials were invalid.”
<!--/issueDescription-->
## **Recommended steps**

To resolve the issue, update the Active Directory user account using the steps as shown in [this article](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-connectors#changing-the-ad-ds-account-password)
