<properties
	  pageTitle="Check if accounts is not eligible to upgrade from Portal"
	  description="Check if accounts is not eligible to upgrade from Portal"
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
	  articleId="02f13345-33c7-40b6-8def-cdcbb1e6b32b"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check if accounts is not eligible to upgrade from Portal

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

#### ** Troubleshooting Accounts that were not eligible to upgrade from Portal**

#### NOTE: Please ensure the customer is using the 3.6 after migration.

1. The update will change the server version. While generally 3.6 is compatible with 3.2, it's recommended a customer try out 3.6 with their application on a dev or qa instance before considering updating the account backing any production workload.
2. Run below query:
```
cluster('cdbsupport').database('Support').AccountAPIProperties ('accountname')
```
If the above query returns **CanMigrateWithoutDataChange** = False, this account cannot be updated in-place (cannot migrate with no downtime).

If the above query returns **CanMigrateWithoutIndexUpgrade** = False, we must spend a few days updating indexes on this account prior to the account update. (cannot migrate immediately, needs prepartion to update indexs)

**IF (CanMigrateWithoutDataChange == True & CanMigrateWithoutIndexUpgrade == True**), it means customer's MongoDB account can be upgraded to v3.6 without downtime and change on the index. Then recommend to the customer to return to the portal and proceed with the self serve for update.


3. If the Customer was not able to migrate using self serve, you will need to file an IcM to MongoDB PG, and once they confirm everything is ready, the actual account update process will take about 5 minutes.
4. Post-update customers will observe in the Portal:
    1. The connection keys will remain the same.
    2. They will have a new connection string, at a different host name (*.mongo.cosmos.azure.com)
    3. The preview features tab will be gone, as there are no preview features associated with 3.6. All previously preview features are GA on 3.6.
4. Their previous connection strings will continue to work, and will continue to act as the 3.2 version of the service. At their convenience they can update their clients to use the new connection strings. 

Please refer to **API-specific Properties** view in ASC to assess readiness or run the below function(by replacing 'accountname') in Kusto Explorer to know more details.



```
cluster('cdbsupport').database('Support').AccountAPIProperties('accountname')
```
|Column|Meaning|
|--|--|
|CanMigrateWithoutDataChange|If False, this account cannot be migrated in-place. The Gridfs or BSON schema compatibility would make this return false|
|CanMigrateWithoutIndexUpgrade|If False, we must update indexes before this account can be migrated. This is transparent to the customer and will not impact existing scenarios, but it will likely take a few days.|

```
cluster('cdbsupport').database('Support').MongoAccountProperties('accountname')
```

|Column|Meaning|
|--|--|
|IsAccountOnCompute|True if the account is already on version 3.6.|
|CommunicationAPIKind|MUST be MongoDB to migrate.|
|EnableBsonSchema|MUST be 1 to migrate. The storage format is not compatible to do in place upgrade. The migration is required.|
|HasIndexV2OnAllCollections|MUST be 1 to migrate.|
|NumGridFSCollections|MUST be 0 to migrate.The storage format is not compatible to do in place upgrade. The data migration is required|

To look at the underlying query for this function, run the following command:

```
.show function MongoAccountProperties
```

**If you need to edit the underlying query, please email Cosmos DB Supportability Team <cosmossupportability@microsoft.com> and they will help you update it since that query is source controlled in ASC repo.**


## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.



<!--/issueDescription-->

