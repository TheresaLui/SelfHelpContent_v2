<properties
	  pageTitle="Consistency - Strong Consistency not Support with 5000 Miles issue"
	  description="Consistency - Strong Consistency not Support with 5000 Miles issue"
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
	  articleId="1aa887fd-58a0-4db5-a459-e2e089ac2ba1"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Consistency - Strong Consistency not Support with 5000 Miles issue

<!--issueDescription-->

Dear customer,

In case you are unable to configure Strong Consistency on a Cosmos DB account with multiple regions configured, please chek the reasons below.

**Azure portal fails with the below message**
*"Strong Consistency account with regions spanning more than 5000 miles is not supported for the target subscription"*
The above error message is thrown when the distance between the regions on account is by 5000 miles.  This behavior is expected  by design.

### Design background
The reason we do not allow it by default, is due to higher network latency which will translate to high latency observed on the account.   
The strong consistency means that the transactions have to be propagated to all region which would lead to high latency.

Strong consistency would mean that the latency would be higher due to network latency between the regions and the transactions have to be propagated to all regions. 

Please review the Strong consistency definition:
https://docs.microsoft.com/en-us/azure/cosmos-db/consistency-levels#guarantees-associated-with-consistency-levels

If you really need to have strong consistency then we can enable it through a configuration request to the engineering team.

Thank you.

<!--/issueDescription-->

