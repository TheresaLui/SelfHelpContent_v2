<properties
	pageTitle="Check if the domain name is verified"
	description="Check if the domain name is verified"
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
	articleId="69ae9126-7fdf-4272-be5e-10ffbc56625a"
/>

# How to check if the domain name is verified

* In order to create a member in Azure AD, the domain name portion of the user name (UPN) must either be a verified domain name in this Azure AD, or the initial *.onmicrosoft.com domain name
* You can typically find the user name for the user that needs to be created as an answer to the scoping questions the customer submitted with the case. 
* You can see the list of verified domain names for the directory in Azure Support Center. 
   * Navigate to Azure AD Explorer, and click on 'Domain names' 
  