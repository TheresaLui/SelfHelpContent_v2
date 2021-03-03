<properties
	pageTitle="Check if the case is assigned the right support topic"
	description="Check if the case is assigned the right support topic"
	service="microsoft.identity"
	resource=""
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="8ca163f3-0942-4ba4-8632-174cf3f6ded1"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the case is assigned the right support topic

1. Most cases filed as user creation, are actually misclassified. 
2. If this case is misclassified, it is important to correct the support topic classification, exit this TSG and, if required, transfer the case to the correct service inside or outside of Identity.
 
## Is this case classified correctly?
 
1. The case is correctly classified if it relates to creating a new user in Azure AD from within the Azure AD administration portal, from MSOL PowerShell cmdlets, or Azure AD PowerShell cmdlets.
2. Choose 'Misroute' below if the case is about other problems, such as inviting B2B guests, users created by Azure AD Connect sync, a provisioning case,  Exchange Online or user creation via the Graph API.

## Misroute cases

1. A case is a B2B case if it involves adding a user:
   1. From another Azure AD tenant
   2. From a consumer email address such as a Microsoft account (such as @outlook.com), or a gmail.com account.
   3. If the case mentions terms like 'invite' or 'redeem', it is a B2B case. Likewise, if the user to be added was initiated from within SharePoint, or while assigning access to an Azure subscription or Azure resource, it is a B2B case.
1. A case is a Provisioning case if it involves adding a user:
   1. who is added to Azure AD by Azure AD Connect sync
   2. who is provisioned from Azure AD into a SaaS application
   3. If the case mentions Windows Server AD, or a SaaS app such as Google apps or Concur, it is a provisioning case.