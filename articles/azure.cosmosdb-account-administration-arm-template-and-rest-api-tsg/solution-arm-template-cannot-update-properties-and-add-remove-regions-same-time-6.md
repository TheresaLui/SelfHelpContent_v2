<properties
	  pageTitle="ARM template Cannot update properties and add remove regions same time"
	  description="ARM template Cannot update properties and add remove regions same time"
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
	  articleId="6e963ab9-2831-423b-9478-8b81ac6eeaa6"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# ARM template Cannot update properties and add remove regions same time

<!--issueDescription-->

Dear customer,

Whenyou add a region and change Consistency Level in the same ARM template, after account is already created using a single region template.

###Example:  
"locations": [
                    {
                        "id": "cosmosarmtest01-eastus2",
                        "failoverPriority": 0,
                        "locationName": "East US 2"
                    },
{
                        "id": "cosmosarmtest01-westus",
                        "failoverPriority": 1,
                        "locationName": "West US"
                    }
                ],
                "enableMultipleWriteLocations": false,
"consistencyPolicy": {
"defaultConsistencyLevel": "Eventual" },

You get a resource creation failure with the following error message:
"New-AzResourceGroupDeployment : 1:21:27 PM - Resource Microsoft.DocumentDB/databaseAccounts 'tstcosmosdb23' failed with message '{
'code': 'BadRequest',
'message': 'Cannot update properties and add/remove regions at the same time. Adding regions 'East US'. Removing regions ''. Attempting to update 'ConsistencyPolicy'\\r\\nActivityId:
d309d68f-62c2-43db-a641-b17ead43ff22, Microsoft.Azure.Documents.Common/2.7.0'
}'"

This is by design. We don't support both AddRegions: {0} or removeRegions: {1}) as well as update settings for the entity.
Also, there are no plans of doing it in future as of now. 

Thank you very much for your comprehension.

<!--/issueDescription-->

