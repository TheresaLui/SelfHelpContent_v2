<properties
	pageTitle="Check if the user is authorized to create a member in Azure AD"
	description="Check if the user is authorized to create a member in Azure AD"
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
	articleId="b0ae7246-672f-4326-be68-931b0ff70685"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the user is authorized to create a member in Azure AD

* In order to create a member in Azure AD, the signed in user must be a global administrator or a user administrator.
* You can find out whether the user is in one of these roles using data in Azure Support Center. 
   * Go to Azure AD Explorer, search for the user, and click on the 'Roles' tab to see the role(s) if any, that the user is in.
* In particular, note that it is a common problem that a user who is a subscription administrator for an Azure subscription, will think that they are authorized to create a new user in Azure AD, even if they are not assigned to an authorized role in Azure AD. 
