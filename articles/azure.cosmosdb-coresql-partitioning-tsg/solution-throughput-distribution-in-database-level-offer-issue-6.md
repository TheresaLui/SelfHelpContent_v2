<properties
	  pageTitle="Throughput distribution in database level offer issue"
	  description="Throughput distribution in database level offer issue"
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
	  articleId="cf14f32d-515a-439a-a0a5-3497ad60be3e"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Throughput distribution in database level offer issue

<!--issueDescription-->

Dear customer

When you provision containers with shared database offering:

- Every 25 containers are grouped into a partition set and the database throughput(D) is shared between the containers in the partition set. If there are up to 25 containers in the database and at any point of time, if you are using only one container, then that container can use a max of (D) throughput.<br>
- For every new container created after 25 containers, a new partition set is created and the database throughput is split between the new partition sets created (that is D/2 for 2 partition sets, D/3 for 3 partition sets). At any point of time, if you are using only one container from the database, it can use a max of (D/2, D/3, D/4 throughput) respectively. Given the reduced throughput, it is recommended that you create no more than 25 containers in one database.<br>
- Please note that there is no throughput allocation or RU load balancing or fairness guarantees across collections

**Example**

- If you create a database named (MyDB) with a provisioned throughput of 10K RU/s <br>
- If you provision 25 containers under (MyDB), then all the containers are grouped into a partition set. At any point of time, if you are using only one container from the database, then it can use a maximum of 10K RU/s (D)<br>
- When you provision 26th container, a new partition set is created and the throughput is split equally between both the partition sets. At any point of time, if you are using only one container from the database, it can use a maximum of 5K RU/s (D/2). Because there are two partition sets, the throughput shareability factor is split into D/2. <br>

Thank you.

<!--/issueDescription-->

