<properties
	pageTitle="Identify command"
	description="Identify command"
	service="Microsoft.DocumentDB"
	resource="databaseAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="c5d8f17d-5194-4d14-83f5-adbfa4365ec5"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Identify command

To identify which command is being executed please run the following  query in Kusto: 

~~~kusto

MongoProxyRequest5M
| where DatabaseAccountName == "<account-name>" and ErrorCode == 16501
| summarize sum(SampleCount) by CommandName

~~~

Please open an ICM ticket against the Cosmos DB MongoDB product team

