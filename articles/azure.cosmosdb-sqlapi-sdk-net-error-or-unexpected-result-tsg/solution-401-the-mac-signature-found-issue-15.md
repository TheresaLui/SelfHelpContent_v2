<properties
	  pageTitle="401 The MAC signature found issue"
	  description="401 The MAC signature found issue"
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
	  articleId="32d31ac4-c744-48a2-8bad-83e96e03f931"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# 401 The MAC signature found issue

<!--issueDescription-->

Dear customer,

If you received the following 401 error message: "The MAC signature found in the HTTP request is not the same as the computed signature," this can be caused by the following scenarios:

* The key was rotated and did not follow the [best practices](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#key-rotation). This is usually the case. Cosmos DB account key rotation can take anywhere from a few seconds to possibly days depending on the Cosmos DB account size.
   * 401 MAC signature is seen shortly after a key rotation and eventually stops without any changes. 
* The key is misconfigured on the application so the key does not match the account.
   * 401 MAC signature issue will be consistent and happens for all calls
* The application is using the [read-only keys](https://docs.microsoft.com/azure/cosmos-db/secure-access-to-data#master-keys).
   * 401 MAC signature issue will only happen when the application is doing write requests, but read requests will succeed.
* There is a race condition with container creation. An application instance is trying to access the container before container creation is complete. The most common scenario for this if the application is running, and the container is deleted and recreated with the same name while the application is running. The SDK will attempt to use the new container, but the container creation is still in progress so it does not have the keys.
   * 401 MAC signature issue is seen shortly after a container creation, and only occur until the container creation is completed.

Thank you.

<!--/issueDescription-->

