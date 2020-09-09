<properties
pageTitle="AAD Connect is configured using an unexpected source anchor"
	description="AAD Connect is configured using an unexpected source anchor"
	infoBubbleText="AAD Connect is configured using an unexpected source anchor"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_InvalidSourceAnchor"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# AAD Connect is configured using an unexpected source anchor
<!--issueDescription-->
AAD Connect is configured using an unexpected source anchor. This can prevent objects from getting synchronized to Azure Active Directory. Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
Resolving this issue will require re-installation of AAD Connect in custom mode. You need to manually select the source anchor attribute. Note that choosing an incorrect source anchor attribute may break the association between on-premises objects and their associated Azure resources.
