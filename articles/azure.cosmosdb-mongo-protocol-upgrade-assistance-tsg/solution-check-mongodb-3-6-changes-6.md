<properties
	  pageTitle="Check MongoDB 3.6 changes"
	  description="Check MongoDB 3.6 changes"
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
	  articleId="f5609887-eb47-4ff6-a657-03bcfdcfba88"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Check MongoDB 3.6 changes

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Just for CSS Information:**
The 40 MB limit is only removed on server version 3.6. It is recommended the customer create a new account on server version 3.6, or request we update this existing account to server version 3.6.

## Example of Customer message:
Dear customer,

#### New Features and Benefits of upgrading to version 3.6:
- Enhanced performance and stability
- Support for new database commands
- Support for aggregation pipeline by default and new aggregation stages
- Cross-partition support for the following operations: UPDATE, DELETE, COUNT, and ORDER BY
- Improved performance for the following aggregate operations: COUNT, SKIP, LIMIT, and GROUP BY
- Changes from previous engine versions
- Support for new commands/aggregation stages added in v3.6
- Support for ChangeStream  (ChangeFeed via changestream)
- Support for Compound indexes
- Support for unsharded collections in databases with throughput.
- Support for aggregate pushdown for Count
- Support for SKIP/LIMIT pushdown
- Support for GROUPBY pushdown for supported queries


#### Changes from v3.2 stack
- Mongo collections will only have _id index by default vs auto-indexing (as with Mongo v3.2 stack)
- Mongo service will not retry on 429s (Mongo v3.2 stack did 10 retries before returning RateLimiting error to client)
- Per request timeout is increased from 15 seconds to 30 seconds

#### **Recommended Documents:**
- https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-feature-support-36
- https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-version-upgrade

Thank you.

<!--/issueDescription-->

