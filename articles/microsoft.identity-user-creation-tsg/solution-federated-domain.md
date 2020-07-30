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


## Root cause

* Users in federated domains can be created in Azure AD only by Azure AD Connect synchronization from an on-premises directory.
 
## Solution

* Create the user in your Window Server AD. 
* Then you will see the user in Azure AD after the next synchronization with Azure AD has completed.
 
## **Recommended Documents**

* [Domain names in the Azure AD administration portal experience](http://todo-add-link.com)
* [Documentation: Creating a user in Azure AD](http://todo-add-link.com)
