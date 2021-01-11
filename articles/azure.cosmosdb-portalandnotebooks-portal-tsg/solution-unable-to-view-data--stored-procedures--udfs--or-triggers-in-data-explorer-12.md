<properties
	  pageTitle="Unable to view data, stored procedures, UDFs, or triggers in Data Explorer"
	  description="Unable to view data, stored procedures, UDFs, or triggers in Data Explorer"
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
	  articleId="dcf2f491-a41f-482e-a94a-06189c5bb025"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Unable to view data, stored procedures, UDFs, or triggers in Data Explorer

<!--issueDescription-->

Dear customer,

If you are not able to view your data including databases, containers, items (documents), stored procedures, UDFs, or triggers from Data Explorer, check if Virtual Networks (VNET) is enabled for your Cosmos account
* If VNET is enabled, navigate to the "Firewall and virtual networks" pane and ensure:
<br>The setting *Allow access from Azure Portal* is enabled

![Check image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EcAgkLlx3nZEvYJ0HYpRNtgBRXvssGUIguvcYUbPEiQtMw?e=bsUpXH)

If you are accessing the Portal from outside the VNET and want to view data, you will need to add your current IP Address to the Firewall. If you are within the VNET, only setting *Allow access from Azure Portal* is required.  

If you have followed these steps and receive a 403 "Unable to proceed with the request. Please check the authorization claims to ensure the required permissions to process the request" error, please contact us for support and provide the ActivityId of the message. The ActivityId can be found in the yellow notification bar at the bottom of the Data Explorer screen. 


**Note** If you do not have permission to view or change VNET/Firewall settings for your account, contact your Cosmos account owner to enable the above.  

Thank you.

<!--/issueDescription-->

