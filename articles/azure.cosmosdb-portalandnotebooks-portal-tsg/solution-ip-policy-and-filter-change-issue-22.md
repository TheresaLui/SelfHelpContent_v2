<properties
	  pageTitle="IP Policy and Filter change issue"
	  description="IP Policy and Filter change issue"
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
	  articleId="9d66f78b-c865-4b32-8dcc-999a84d76fb0"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# IP Policy and Filter change issue

<!--issueDescription-->

Dear customer,

The IP filter for Azure portal is getting more restrictive based on various customer asks toward securing the data access in Azure Cosmos DB.  

#### New/Changed Behavior
The way Data Explorer accesses your databases and containers has changed.


#### Effected Operations
- Documents Access
- Modify the databases and container
- Settings

You need to update your Firewall settings to add your current client IP address to the firewall rules.  Please open Firewall blade in Azure portal, click ?Add my IP address? and click ?Save?.

**Note** that firewall policy updates may take up to 15min to propagate. If for some reason you are unable to update firewall settings, please contact your Cosmsos DB account owner


The Portal would show the below Notification/Advisory. 
<br>
![Notification image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EfAcf19Zxg9LvMetgnYWJGwBjPzyNC5t90QqsuiVQ8rw9w?e=KaDoSx)


**Old Behavior**  
The IP Filter Access Policy restricts access to data from non-whitelisted IPs.  Access from Azure Portal needs to be enabled by setting the option ?Allow access from Azure Portal? as shown below.  This option basically adds the list of IP for Azure portal. 

![Old Behavior image](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EdI9Gx9NjgdDuqVgRn0hKpcB0nqg0MQnf4l349oI27bN1A?e=DRTzED)

Thank you.

<!--/issueDescription-->

