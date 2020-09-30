<properties
	pageTitle="Check what is reason for the request malformed category"
	description="Check what is reason for the request malformed category"
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
	articleId="19b623f9-92ac-4b64-a3c4-6a2f5df10b1d"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check what is reason for the request malformed category

Native MongoDB support the quotation mark in the NumberLong(): [Data Types](https://docs.mongodb.com/manual/core/shell-types/)

Current Cosmos DB doesn't support quotation mark in NuberLong(), there is bug tracking the issue

Until quotation mark is supported in NumberLong() by Cosmos DB recommend to customer to remove them, insert should then succeed

Provide customer with ready message below.
