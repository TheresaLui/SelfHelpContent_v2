<properties
	pageTitle="Check Kusto for admin portal errors"
	description="Check Kusto for admin portal errors"
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
	articleId="4c3764b1-75ed-4188-9912-b6fc62d38662"
	   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check Kusto for admin portal errors

* Use Kusto to look for errors for requests in the Azure AD admin portal experience, initiated by the admin who is trying to create a user.

~~~kusto 

https://idsharedwus.kusto.windows.net:443/ADIbizaUXWUS 
// Determine all calls made by the user. Calls with responseCode >=400 signifies a failure
IfxRequestOperationResultScrubbed
| where operationName contains "CreateUser"
| where env_time > datetime(YYYY-MM-DD hh:mm:ss) and env_time < datetime(YYYY-MM-DD hh:mm:ss) // Remove if timestamp of the issue is not available.
| where tenantId contains "$Tenant Id$" // Remove if tenantId is not available
| where userObjectId contains "$User Object Id$" // Remove if userObjectId is not available
| project env_time, operationName, resultSignature, responseCode, , correlationId, sessionId  // Add more columns to display

~~~
