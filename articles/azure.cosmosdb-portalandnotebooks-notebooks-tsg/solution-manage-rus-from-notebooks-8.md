<properties
	  pageTitle="Manage RUs from Notebooks"
	  description="Manage RUs from Notebooks"
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
	  articleId="ffdff041-c4ba-492b-8d9a-b151772c4f85"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Manage RUs from Notebooks

<!--issueDescription-->

Dear customer,

There are cases in which the scaling operation needs to be done through data bricks notebooks. The sample provided below would help to scale up or down the provisioned throughput.

#### Requirement: Install PyPI package on the Cluster.

![Image Sample](https://microsofteur-my.sharepoint.com/:i:/g/personal/anferrei_microsoft_com/EU3XTyktyOpFuUBcwusx1j4BuQnlCjdZg1p2b_VLIkwMnA?e=DmOTQy)

#### Sample Code

```
import azure.cosmos.cosmos_client as cosmos_client
def create_collection_if_not_exists(cosmosEndpoint, cosmosKey, databaseName, collectionName, InitialThroughput, UpdatedThroughput):
    client = cosmos_client.CosmosClient(url_connection=cosmosEndpoint, auth={'masterKey': cosmosKey})


    db = client.QueryDatabases("select * from c where c.id = '" + databaseName + "'").fetch_next_block()[0]
    options = {
      'offerThroughput': InitialThroughput
    }


    container_definition = {
      'id': collectionName,
       "partitionKey": {  
         "paths": [  
            "/id"  
         ],  
         "kind": "Hash" 
       },
      "indexingPolicy": {  
        "indexingMode": "consistent",  
        "automatic": True,  
        "includedPaths": [],  
        "excludedPaths": [{
          "path": "/*"
        }]  
      }
    }
    
    container = client.CreateContainer(db['_self'], container_definition, options)
    
    database_link = 'dbs/' + databaseName
    collection_link = database_link + '/colls/{0}'.format(collectionName)
    collection = client.ReadContainer(collection_link)
    
    offer = list(client.QueryOffers('SELECT * FROM c WHERE c.resource = \'{0}\''.format(collection['_self'])))[0]
            
    print('Found Offer \'{0}\' for Collection \'{1}\' and its throughput is \'{2}\''.format(offer['id'], collection['_self'], offer['content']['offerThroughput']))
    
    offer['content']['offerThroughput'] = UpdatedThroughput
    offer = client.ReplaceOffer(offer['_self'], offer)


    print('Replaced Offer. Offer Throughput is now \'{0}\''.format(offer['content']['offerThroughput']))
    
```

Thank you.

<!--/issueDescription-->

