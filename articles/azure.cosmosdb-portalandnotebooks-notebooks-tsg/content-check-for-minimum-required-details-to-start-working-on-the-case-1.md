<properties
	  pageTitle="Check for minimum required details to start working on the case"
	  description="Check for minimum required details to start working on the case"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="da1a96a8-ecd5-4786-8a2b-3383128a79a2"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check for minimum required details to start working on the case

Review customer verbatim and validate that the case has the minimum required details mentioned below to start working. Most of the information should have been already provided in the scoping questions. 

1. Clear issue description
2. Subscription ID
3. When did the problem begin?
4. Account name
5. Database name 
6. Collection name
7. What changes were made? (if applicable)
8. Error message/StackTrace (if applicable)
9. HAR file (see how to obtain below)

**Please try to obtain all the information from ASC Resource Explorer before reaching the customer.**

If no enough details, please provide customer with customer ready message for minimum required details to start the case.
#Required Details:

**Get a HAR file from Customer:**
Use [F12] to open the developer tools in your browser. Navigate to the Network tab. Reproduce the issue, while the network requests are being recorded. Save the network traces as a HAR file: in Chrome or Firefox, right-click inside the network pane of requests and select 'Save all as HAR'; in Edge or Internet Explorer, select the 'Export as HAR' command or type [Ctrl] + [S] in the Network tab.

## Additional Details to assist on Capture browser network HAR File:
1. Hit F12 on your browser
2. Refresh browser (F5) - This will clear session caches
3. Reproduce the issue
4. export network trace as HAR file
5. Chrome and new Edge
6. Right click on network log entries
7. Select "Save all as HAR with content"
