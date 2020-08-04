<properties
	pageTitle="Check if the domain is federated"
	description="Check if the domain is federated"
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
	articleId="c9ddffd4-24ba-4a46-9c69-7a673e8bb758"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check if the domain is federated

1. In order to create a member in Azure AD, the domain name portion of the user name (UPN) must not be a domain name for which federation has been configured with Azure AD, such as using Active Directory Federation Services (AD FS).
2. You can see if a domain name is federated in Azure Support Center. 
   1. Navigate to Azure AD Explorer, and click on 'Domain names' and look in the 'Type' column for the domain name. 
  
