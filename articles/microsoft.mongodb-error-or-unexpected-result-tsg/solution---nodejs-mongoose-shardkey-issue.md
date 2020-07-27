<properties
	pageTitle="NodeJs Mongoose shardKey issue"
	description="NodeJs Mongoose shardKey issue"
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
	articleId="093092c2-5fd7-4357-9a41-72ad4b542d61"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# NodeJs Mongoose shardKey issue

<!--issueDescription-->

Dear customer,

You have 2 options to solve this issue: 
1. You should create the collection manually with the desired shardKey using one of the two following methods using Mongo shell, use the shardCollection command i.e. db.adminCommand({shardCollection:"<database>.<collection>", key:{"<shardkey>":"hashed"}})
https://docs.mongodb.com/manual/reference/command/shardCollection/ 
-OR-
Create the collection through the portal and there specify the shard key
2. You should specify the shardkey in the Mongoose schema i.e. ( new Schema({tag: String, .. }, { shardKey: { tag: 1 }}))
https://mongoosejs.com/docs/guide.html#shardKey 
3. You should specify the collection name to be the same as set in the portal or shell i.e. ( new Schema({tag: String, .. }, { shardKey: { tag: 1 }, collection: "name"}))
https://mongoosejs.com/docs/guide.html#collection 

# Additional Information

This occurs because Mongoose will not send the shardCollection command and recommends users create the sharded collections manually (https://mongoosejs.com/docs/guide.html#shardKey )

Thank you.

<!--/issueDescription-->

