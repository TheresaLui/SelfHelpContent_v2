<properties
	  pageTitle="Customer using MongoDB version 3.2"
	  description="Customer using MongoDB version 3.2"
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
	  articleId="d5e58011-8180-49f3-85be-22c5ef82f54f"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Customer using MongoDB version 3.2

<!--issueDescription-->

Dear customer,

I would like to mention that your account is using version 3.2, and now we do have an updated version of 3.6. Updating to 3.6 would help in this scenario. 

Upgrading to the latest version of the service will provide the most up to date functionality, as well as enhancements in performance, stability, and the latest fixes.

The upgrade process will not provide any service interruptions or downtime. It will also not require any data or index migrations. As soon as you start the process, your account will be queued to proceed with the upgrade. You will be notified when your account has finished upgrading.

Benefits of upgrading to version 3.6:
. Enhanced performance and stability
. Support for new database commands
. Support for aggregation pipeline by default and new aggregation stages
. Support for ChangeStream
. Support for Compound Indexes
. Cross-partition support for the following operations: UPDATE, DELETE, COUNT, and ORDER BY
. Improved performance for the following aggregate operations: COUNT, SKIP, LIMIT, and GROUP BY
. Changes from previous engine versions

MongoDB collections will only have the _id property indexed by default

Action Required:
The connection string to the MongoDB service in your application will need to be updated as shown in the Overview dashboard of the Azure Portal. The updated endpoint is: ACCOUNTNAME.mongo.cosmos.azure.com but it might differ if your account is in a Sovereign, Government, or Restricted Azure cloud.

Please let me know your feedback on the above.
 
Thank you.

#Recommended Documents
https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-version-upgrade
https://devblogs.microsoft.com/cosmosdb/upgrade-your-server-version-from-3-2-to-3-6-for-azure-cosmos-db-api-for-mongodb/
https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support-36
https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support
https://docs.microsoft.com/en-us/azure/cosmos-db/connect-mongodb-account

<!--/issueDescription-->

