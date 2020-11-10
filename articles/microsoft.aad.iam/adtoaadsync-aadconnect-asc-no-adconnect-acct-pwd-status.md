<properties
	pageTitle="ADtoAADSync_AADConnect_ASC_No_ADDSConnectAcctPwdStatus"
	description="The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS connector"
	infoBubbleText="The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS Connector. See details on the right."
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="aditis"
	ms.author="SahaAditi"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_No_ADDSConnectorAcctPwdStatus"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# The Active Directory account password has been changed but it has not been updated on the synchronization service AD DS connector
<!--issueDescription-->
We have detected that the Active Directory (AD) account password on your Azure AD Connect server has been changed but it has not been updated on the synchronization service AD DS connector. As a consequence, the synchronization service will no longer be able to import/export changes to on-premises.
<!--/issueDescription-->

## **Recommended Steps**

* [Update the Active Directory user account](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnectsync-service-manager-ui-connectors#changing-the-ad-ds-account-password)
