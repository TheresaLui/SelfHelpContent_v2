<properties
	pageTitle="Aggregrate query"
	description="Aggregrate query"
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
	articleId="2cbe0608-03c5-40df-9ceb-8cf6e9fb3329"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Aggregrate query

<!--issueDescription-->

Dear customer, 

To resolve the issue:
1. Get the aggregate query that is being executed
2. Does the aggregate query contain a $match stage as the first stage
    If yes, this means that the query is not selective enough to limit of documents loaded. Please check if you can add more filters to reduce the size
    If no, Query is loading all the documents in the collection to do grouping. Please check if you can add a $match filter to reduce the number of documents loaded.
    Please also check the number of documents in the collection, the number of documents which would match the filter provided in match stage This is possible by converting the query to find().itcount() e.g. db.test.aggregate([{match:**{a:1}**}, {$sort: {b:-1}}]) query can be converted to db.test.find(**{a:1}**, {_id:1}).itcount()

Only the highlighted portion from the aggregate query should be copied over to the find() query.
3. Does the aggregate query contains only $match, $sort, $project stages (any combination of these stages)?
    If the query contains any/all of these stages (AND NO OTHER STAGE), then we suggest moving to the find() command instead of aggregate() for better query performance. The format of the find() command is documented at https://docs.mongodb.com/manual/reference/method/db.collection.find/  

<!--/issueDescription-->

