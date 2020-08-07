<properties
pageTitle="Password Hash Synchronization may not be working for some domains"
	description="Password Hash Synchronization may not be working for some domains"
	infoBubbleText="Password Hash Synchronization may not be working for some domains"
	service="microsoft.aad.iam"
	resource="aadconnect"
	authors="rodejo"
	ms.author="rodejo"
	displayOrder="1"
	articleId="ADtoAADSync_AADConnect_ASC_PhsIsDomain"
	diagnosticScenario=""
	selfHelpType="Diagnostics"
	resourceTags=""
	productPesIds="16666"
  cloudEnvironments="public, Fairfax, Mooncake, ussec, usnat"
  ownershipId="AzureIdentity_AzureActiveDirectoryConnect"
/>

# Password Hash Synchronization may not be working for some domains
<!--issueDescription-->
Password Hash Synchronization is incorrectly skipping some domain(s). This is happening due to a product bug where these domain(s) are flagged with IsDomain=false. Details: <!--$IssueDetails-->[IssueDetails]<!--/$IssueDetails-->
<!--/issueDescription-->

## **Recommended Steps**
To resolve this issue, you need to verify that the AD partition is set correctly and subsequently fix the IsDomain flag in AD connector configuration. Please see link below for detailed instructions.
