<properties
	  pageTitle="Returns No documents found"
	  description="Returns No documents found"
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
	  articleId="64dcf298-3ba3-4302-a972-fd098b6a06fe"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Returns No documents found

<!--issueDescription-->

Dear customer,

**Symptom**: Document Explorer returns No documents found

**Solution:** Ensure that you have selected the correct subscription, database and collection in which the documents were inserted. Also, check to ensure that you are operating within your throughput quotas. If you are operating at your maximum throughput level and getting throttled, lower application usage to operate under the maximum throughput quota for the collection.

**Explanation**: The portal is an application like any other, making calls to your DocumentDB database and collection. If your requests are currently being throttled due to calls being made from a separate application, the portal may also be throttled, causing resources not to appear in the portal. To resolve the issue, address the cause of the the high throughput usage, and then refresh the portal blade. Information on how to measure and lower throughput usage can be found in the [Throughput](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips#measure-rus) section of the [Peformance tips](https://docs.microsoft.com/en-us/azure/cosmos-db/performance-tips) article.

Thank you.

<!--/issueDescription-->

