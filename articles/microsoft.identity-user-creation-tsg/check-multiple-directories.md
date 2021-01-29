<properties
	pageTitle="Check if this case involves an admin of multiple directories"
	description="Check if this case involves an admin of multiple directories"
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
	articleId="2eb4c504-f4ff-41ee-a86a-0e9998977dec"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if this case involves an admin of multiple directories

1. Example scenario
   1. contoso.com is a verified domain name in one Azure AD tenant, and contoso-europe.com is a verified domain name of another Azure AD tenant.
   2. alice@contoso.com is a global administrator of both contoso.com, and contoso-europe.com
   3. alice@contoso.com wants to add bob@contoso-europe.com, as a user within the contoso.com directory
2. That is, the administrator is attempting to add a user in one directory, when the user to be added already exists in another directory of where the administrator is assigned to an admin role.

## Recommended Steps

1. You can evaluate this in Azure Support Center.
   1. Add the tenant by entering the name of the other directory (like 'contoso-europe.com') in the left nav bar within Azure AD explorer
   2. If the tenant exists, search in that directory for the admin who is trying to add the user in the other directory (like 'alice@contoso.com')
   3. If the admin exists in that tenant, then the problem fits the special pattern.
