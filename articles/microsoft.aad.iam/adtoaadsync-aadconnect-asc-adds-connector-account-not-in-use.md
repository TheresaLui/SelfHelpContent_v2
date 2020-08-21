<properties
pageTitle="Autocreated AD DS Connector Account is not being used"
	description="Autocreated AD DS Connector Account is not being used"
	infoBubbleText="Autocreated AD DS Connector Account is not being used"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_ADDS_Connector_Account_Not_In_Use"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Autocreated AD DS Connector Account is not being used
<!--issueDescription-->
The auto created AD DS Connector Account is not being used.
<!--/issueDescription-->

## **Recommended Steps**
It is preferable to choose the autocreated AD DS Connector Account instead of a user provided AD DS Connector Account given that the later requires to manually grant the correct permissions so the feature(s) can work properly. Changing the AD DS Connector Account requires reinstalling AADConnect.
