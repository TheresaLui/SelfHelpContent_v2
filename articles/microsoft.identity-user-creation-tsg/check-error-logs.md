<properties
	pageTitle="Check error logs"
	description="Check error logs"
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
	articleId="04f4da24-cb9e-41b6-ab51-0da7cb524a73"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check error logs

1. Many customer questions about user creation can be answered by looking at the audit logs in Azure Support Center.
2. To find requests having to do with user creation, go to the audit logs in Azure Support Center. 
   1. Set the time range that corresponds to the time when the customer indicated the problem began. 
   2. Put the words “Add user” into the filter box for Action.
   3. Enter the user name object ID for the requestor into the ‘Actor’ column. 
   4. You may find it helpful to filter down to requests that were failed. 
   5. You can find information about the request in the JSON document.
 