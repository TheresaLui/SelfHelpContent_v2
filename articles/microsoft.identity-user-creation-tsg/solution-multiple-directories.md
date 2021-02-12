<properties
	pageTitle="Domain can not be verified in multiple Azure AD instances"
	description="Domain can not be verified in multiple Azure AD instances"
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
	articleId="bb96b3d5-19dc-45bc-a165-7635164a0072"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Domain can not be verified in multiple Azure AD instances
 
 <!--issueDescription-->
 
### Root Cause

1. A user created in Azure AD can only have a domain name that has previously been added and verified in that Azure AD. 
2. A domain name can be verified in only one Azure AD at a time.
 
### Solution 1

1. To create a user whose user name contains ‘contoso.com’, you will to delete that domain name from the other Azure AD (contoso.onmicrosoft.com). 
2. Then you can verify it in contosoltd.onmicrosoft.com, and add users with user names like ‘alice@contoso.com.’
 
### Solution 2

1. You can create a user whose user name contains a domain name that is already available for use in your Azure AD, e.g., ‘alice@contoso.onmicrosoft.com.’
 
### Solution 3

1. You can invite a user from the other directory as a B2B guest in your directory. 
2. The B2B guest user’s credential would remain under the control of the administrators of that other directory.
 
 <!--/issueDescription-->

## Recommended Documents

* [Domain names in the Azure AD administration portal experience](http://todo-add-link.com)
* [Documentation: Creating a user in Azure AD](http://todo-add-link.com)
* [Documentation: Adding and verifying a domain name](http://todo-add-link.com)
 