<properties
	  pageTitle="Consistency - Update Default Consistency Error issue"
	  description="Consistency - Update Default Consistency Error issue"
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
	  articleId="e816d442-a5be-42d8-a9d0-194995d3a3b4"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Consistency - Update Default Consistency Error issue

<!--issueDescription-->

Dear customer,

In case your Cosmos DB account has configured VNET on it and there is an AAD user who has the Contributor Role for the Cosmos DB resource but only Reader Role for the VNET resource.

If the AAD user wants to change the 'Default Consistency', will meet error as below:
https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EYczWSxkH2RNlMu_d100hE4B_s43Nfqn9yBFWRFkL9MU9w?e=gFhOqx

Or change some other configuration of Cosmos DB, will meet below error:
https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EZyjYw-WvClNjAymsSqqPJEB-Xw-lIP6ajCd5CD5iTGXPA?e=gEIxMR

The solution is to Remove the VNET settings  or Change the Reader Role to the Network Contributor Role for the VNET resource.

**Note:**  
If the AAD user is assigned a custom role for the VNET resource, the custom role needs to add permissions: 

This permission allows users to add Cosmos DB Account  to VNET/subnet but no actions on VNET/subnet  
*?Microsoft.Network/virtualNetworks/subnets/joinViaServiceEndpoint/action?*

This permission is to update VNET coniguration for Cosmos DB Account  
*"Microsoft.DocumentDB/databaseAccounts/write"*
[Document about how to create custom role](https://docs.microsoft.com/en-us/azure/role-based-access-control/custom-roles)

**Cause:**  
When updating consistency level, it also needs to pass the existing virtual network rules to ARM. Because we don't support PATCH in ARM yet, so every time customer is trying to update some property, all the existing properties need to be passed. So in this case, even though customer is only updating the consistency level for Cosmos DB account, ARM will validate whether user has permission *"Microsoft.Network/virtualNetworks/subnets/joinViaServiceEndpoint/action"*

Thank you.

<!--/issueDescription-->

