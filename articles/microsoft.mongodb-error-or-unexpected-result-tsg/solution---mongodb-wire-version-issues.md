<properties
	pageTitle="MongoDB wire version issues "
	description="MongoDB wire version issues "
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
	articleId="7556bc9b-1694-4887-86c6-b670bba7dd39"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# MongoDB wire version issues 

<!--issueDescription-->

Dear customer,

You can communicate with the Azure Cosmos DB's API for MongoDB using any of the open-source MongoDB client drivers. The Azure Cosmos DB's API for MongoDB enables the use of existing client drivers by adhering to the MongoDB [wire protocol](https://docs.mongodb.com/manual/reference/mongodb-wire-protocol/).

Some versions of MongoDB drivers require the initial handshake include a minimum wire protocol version. 

Accounts on server version 3.6, the drivers should work with no change required
Accounts on server version 3.2, if the driver throws an error related to the wire protocol version, try enabling the preview feature for wire protocol version 3.4 and appending an appName identifying the account to the connection string: &appName=@accountName@

Thank you.

<!--/issueDescription-->

