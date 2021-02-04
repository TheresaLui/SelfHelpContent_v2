<properties
	  pageTitle="Check Recommended Steps"
	  description="Check Recommended Steps"
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
	  articleId="4b5f449d-3520-46d7-9cb0-1f9f4d483796"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check Recommended Steps

Make sure customer provides Session Id and HAR file:

**Get Session ID:**    
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

