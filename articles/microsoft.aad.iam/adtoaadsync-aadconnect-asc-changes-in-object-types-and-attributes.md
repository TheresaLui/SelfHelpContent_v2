<properties
pageTitle="Connector attributes and/or object types have been modified in Sync UI"
	description="Connector attributes and/or object types have been modified in Sync UI"
	infoBubbleText="Connector attributes and/or object types have been modified in Sync UI"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_Changes_In_Object_Types_And_Attributes"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Connector attributes and/or object types have been modified in Sync UI
<!--issueDescription-->
We have detected that at least one machine associated to this tenant has connectors whose attributes and/or object types have been modified in the Sync UI (Old UI). Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
When changing the object type/attribute inclusion list on a Connector using the Sync UI (Old UI) the currently configured Synchronization Rules are at risk of getting out of sync. Please have in mind that there could be errors. Ideally, changes to attributes should be performed in the AADConnect Wizard and changes to object types should follow the recommended practices for object filtering.
