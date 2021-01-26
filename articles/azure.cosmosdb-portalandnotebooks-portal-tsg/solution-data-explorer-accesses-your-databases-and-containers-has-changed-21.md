<properties
	  pageTitle="Data Explorer accesses your databases and containers has changed"
	  description="Data Explorer accesses your databases and containers has changed"
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
	  articleId="89e9bfcf-0a3b-48ee-baac-448aad56688f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Data Explorer accesses your databases and containers has changed

<!--issueDescription-->

Dear customer,

**Issue:** You are trying to access your objects in Data Explorer and are getting the message: "The way Data Explorer accesses your databases and containers has changed.  You need to update your Firewall settings to add your current IP address to the firewall rules.  Click here, then click 'Save'.  Should you run into any issues access your data via https://cosmos.azure.com (or click 'Full Screen' below)."

**Investigation**:
Do you have any firewall or VNET settings?  If yes, please continue checking this. 

However, if you only have **All Networks** or checking firewall and VNET does not resolve the issue, please try the following:

Using developer tools obtain a HAR file. Select the console. Look for something similar to ?resource token expired due to time? or resource token is no longer valid?? 

**Solution**: If you find one of these items in the HAR  file, it's possible the your PC time is several hours off. Once the time is correctly synced on the device, you should be able to access the databases and collections. 

Thank you.

<!--/issueDescription-->

