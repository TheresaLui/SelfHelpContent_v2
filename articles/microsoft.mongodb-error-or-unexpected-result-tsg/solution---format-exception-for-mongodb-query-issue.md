<properties
	pageTitle="Format Exception for MongoDB query issue"
	description="Format Exception for MongoDB query issue"
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
	articleId="cfc50f96-0d71-4674-994d-18e99b430d31"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Format Exception for MongoDB query issue

<!--issueDescription-->

The issues occurs when customer (or application) inserts a document through endpoint other then mongo like SQL api/ASA/Azure Functions.

Please reach out to the customer to check with the customer if the collection being accessed by applications other then Mongo. If yes, please respond the customer with following details (Please feel free to restructure the message if you like)

#Example of Exception trace#:
```
Format exceptionEventName="MessageEvent" Message="MongoProxy: Unknown error System.FormatException: Value is expected to be an object instead it was 'String', propertyName 'id' - "_rid": "qYwYAILcLQQBAAAAAAAAAA==" at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.CosmosBsonReader.ThrowFormatException(String format, Object[] args) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.CosmosBsonReader.ReadBsonType() at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertJsonDocument(CosmosBsonReader reader, Int32 depth, BsonDocument& bsonDocument) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertJsonValue(CosmosBsonReader reader, Int32 depth, BsonValue& value) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertToBsonPrivate(String jsonDocument, BsonValue& bsonValue, Boolean retainSystemProperties, Boolean processTTLField) at Microsoft.Azure.Documents.Interop.Mongo.Common.BsonExtensions.ToMongoDBFormat(Document docDbDocument, Boolean enableBsonSchema, Boolean processTTLField, Boolean useLegacyUuidSerializationOrder) at Microsoft.Azure.Documents.Interop.Mongo.RequestHandlers.QueryHandler.<QueryAsync>d__0.MoveNext() --- End of stack trace from previous location where exception was thrown --- at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) at Microsoft.Azure.Documents.Interop.Mongo.MongoCommandProcessor.<QueryAsync>d__3.MoveNext() --- End of stack trace from previous location where exception was thrown ---
```

Provide customer with ready message below.

Dear customer,

You cannot use Cosmos DB SDKs to add documents to a Mongo account. This is blocked on newer accounts, however, if the account is old enough that the block is not present. You must delete the documents you added using the Cosmos DB SQL SDK, using that SDK. They will not be retrievable through the Mongo API. Use Mongo SDKs/drivers to insert documents to Mongo accounts.

<!--/issueDescription-->
