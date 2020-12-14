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
	  articleId="d66347c8-a6db-4577-b20f-b7f3524529a0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check for minimum required details to start working on the case

Review customer verbatim for the following and validate that the case has the minimum required details to start working:

1. Clear issue description
2. Subscription ID
3. When did the problem begin?
4. Account name
5. Database name 
6. Collection name
7. Account location
8. Is the error persistent or intermittent? 
9. What changes were made?
10. Error message/StackTrace
11. Attachments (if applicable)
12. ActivityId (if applicable)
13. Get HAR file
14. Session Id

If no enough details, please provide customer with customer ready message for minimum required details to start the case.

#Required Details:

**Get Session Id:**    
Ctrl+Alt+A - Once the Portal has loaded, hit "Ctrl+Alt+A" which will provide information about what subscriptions are currently loaded, timestamps, and a bunch of other stuff that might be useful.  One of the most helpful pieces is the **sessionId**, which we
can use to filter users session.

**Get a HAR file from Customer:**
Use [F12] to open the developer tools in your browser. Navigate to the Network tab. Reproduce the issue, while the network requests are being recorded. Save the network traces as a HAR file: in Chrome or Firefox, right-click inside the network pane of requests and select 'Save all as HAR'; in Edge or Internet Explorer, select the 'Export as HAR' command or type [Ctrl] + [S] in the Network tab.

##Additional Details to assist on Capture browser network HAR File:
1. hit F12 on your browser
2. Refresh browser (F5) - This will clear session caches
3. Reproduce the issue
4. export network trace as HAR file
5. Chrome and new Edge
6. right click on network log entries
7. Select "Save all as HAR with content"
