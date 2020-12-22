<properties
	  pageTitle="Understanding TTL behavior and tracking issue"
	  description="Understanding TTL behavior and tracking issue"
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
	  articleId="788be2ef-8198-439a-8cae-fce5856da5b1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Understanding TTL behavior and tracking issue

<!--issueDescription-->

Dear customer, 

The objective of TTL Setting is as follows
* Purge Expired documents/attachments automatically
* The expired document would be hidden for the users
* Purging is done in the background in using left over RU from the User Workload. So, no impact to user workload
* The Quota size is calculated excluding the expired document

Setting Options:
| SL | Setting         | Description                                                                                                                                                           |
|----|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1  | Off             | The Container Level the TTL is switched off.  Complete disable of TTL even if the item has TTL property set                                                           |
| 2  | On (no default) | This option enables the TTL for the container with value as -2 which means the item level property is looked to purge the document.                                   |
| 3  | On              | This options takes a value in seconds which is used to purge the document at the container level.  But the item level property TTL does override the container level. |

We suggest you to go throught the FAQ below to better understand the TTL behavior in Cosmos DB.

**When Does TTL Does not Work?**  
TTL would not apply when the Index is set to NONE

**How to Set TTL on Document or at Item Level**  
The user can set TTL on a document when creating a new document or replacing an existing document by specifying TTL property in the document.  https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-time-to-live#set-time-to-live-on-an-item

**How to Clear TTL on Document or at Item Level**  
The user can set TTL on a document by passing special value "-1" https://docs.microsoft.com/en-us/azure/cosmos-db/how-to-time-to-live#disable-time-to-live

**How to find the Current TTL Settings**  
Use the Default TTL Value from Query from "How to find the Status of the Purging" Section  
or  
TSG Admin: How to find the Collection Settings /Index Policy/ Partition Key/TTL Settings/

**When does the Purging Takes Place**  
The TTL Setting is evaluated by a back ground track and does the purging asynchronously.  Please refer the Purging Status Section for tracking the Purging

**Does Purging consume the User Provisioned RU? If so, does it impact customer workload? What Percentage of RU would be consumed? How?**  
Purging does not impact user workload.   The purging uses the left over RU and does not run when the User workload is consuming the provisioned RU

**What is the best practice TTL Setting for Collection? Would it help by setting progressively?**  
There are two phase when the TTL is set.  The evaluation phase to identify the document which are eligible for purging which would be a scan.  So it would be better if we configure the TTL once instead of multiple times.

**Is there a way to faster the purging timeline?**  
Increasing the Provisioned RU would help to have more leftover RU which would help the purging to perform faster

**Does ALL Cosmos DB API Support TTL?**   
Mongo, please refer to: https://docs.microsoft.com/en-us/azure/cosmos-db/mongodb-time-to-live. 
Table/Cassandra/Graph at the Container Level

**Why the data re-appears if the TTL was reset to higher Value?**  
Let say the TTL was set to 1 minutes at 12:00 PM and immediately  after the TTL is reverted back to say 1 hour or larger value.  The Data would reappear since the TTL has two phase, the phase one does evaluate the document to list the eligible document to be archived.  The actual archival occurs asynchronously.  So, changing the TTL immediately to a higher TTL would lead the documents to reappear.

**What is the isolation behavior for a Query submitted after enabling the TTL?**
**Example:**
Time 1 Collection has 100K Document  
Time 2 TTL is enabled  
Time 3 TTL is in the process of purging which archive 50K document  
Time 4 A Query is submitted while the purging is occurring. The query would match all the 100k Document  

**Expected Result :**  The Query would result 50K+ document and may not return all document since the purging might have removed some document. So the result might be greater than 50K and not all 100 K

Please let us know if you have any question or concern.

Thank you.


<!--/issueDescription-->

