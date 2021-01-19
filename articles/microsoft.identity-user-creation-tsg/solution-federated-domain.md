<properties
	pageTitle="Users can not be created in federated domain"
	description="Users can not be created in federated domain"
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
	articleId="fbb1c152-be96-46fd-8229-97b4e359d445"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Users can not be created in federated domain

<!--issueDescription-->
### Root cause

1. Users in federated domains can be created in Azure AD only by Azure AD Connect synchronization from an on-premises directory.
 
### Solution

1. Create the user in your Window Server AD. 
2. Then you will see the user in Azure AD after the next synchronization with Azure AD has completed.
 
 <!--/issueDescription-->

## Recommended Documents

1. [Domain names in the Azure AD administration portal experience](http://todo-add-link.com)
2. [Documentation: Creating a user in Azure AD](http://todo-add-link.com)
