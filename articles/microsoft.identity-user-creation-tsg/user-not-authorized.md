<properties
	pageTitle="User is not authorized to create users in Azure AD"
	description="User is not authorized to create users in Azure AD"
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
	articleId="20d5f5fd-9e1f-47cc-881d-655a71124d7e"
/>

# User is not authorized to create users in Azure AD
 
## Root Cause

* Users can only be created in Azure AD by users who are assigned to the Global administrator or User administrator roles. The user is not assigned to either of these roles.
 
## Solution 

* You can ask an administrator to create the new user for you. Alternatively, you can ask a global administrator to add you to either the Global administrator role or the User administrator roles.
 
## **Recommended Documents**

* [Roles and administrators in the Azure AD administration portal experience](http://todo-add-link.com)
* [Documentation: Administrative role permissions in Azure AD](http://todo-add-link.com)
 