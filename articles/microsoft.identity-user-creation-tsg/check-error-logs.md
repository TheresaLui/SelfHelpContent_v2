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
/>

# How to check error logs

* Many customer questions about user creation can be answered by looking at the audit logs in Azure Support Center.
* To find requests having to do with user creation, go to the audit logs in Azure Support Center. 
   * Set the time range that corresponds to the time when the customer indicated the problem began. 
   * Put the words “Add user” into the filter box for Action.
   * Enter the user name object ID for the requestor into the ‘Actor’ column. 
   * You may find it helpful to filter down to requests that were failed. 
   * You can find information about the request in the JSON document.
 