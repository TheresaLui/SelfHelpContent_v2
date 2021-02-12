<properties
	pageTitle="Check with the customer if the collection being accessed by applications other then MongoDB drivers"
	description="Check with the customer if the collection being accessed by applications other then MongoDB drivers"
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
	articleId="cb3d2365-1f1b-45b6-ac8d-8dc4caf422f9"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check with the customer if the collection being accessed by applications other then MongoDB drivers

The issues occurs when customer (or application) inserts a document through endpoint other then mongo like SQL api/ASA/Azure Functions.

Please reach out to the customer to check with the customer if the collection being accessed by applications other then Mongo. If yes, please respond the customer with following details (Please feel free to restructure the message if you like)

#Example of Exception trace#:
```
Format exceptionEventName="MessageEvent" Message="MongoProxy: Unknown error System.FormatException: Value is expected to be an object instead it was 'String', propertyName 'id' - "_rid": "qYwYAILcLQQBAAAAAAAAAA==" at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.CosmosBsonReader.ThrowFormatException(String format, Object[] args) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.CosmosBsonReader.ReadBsonType() at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertJsonDocument(CosmosBsonReader reader, Int32 depth, BsonDocument& bsonDocument) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertJsonValue(CosmosBsonReader reader, Int32 depth, BsonValue& value) at Microsoft.Azure.Documents.Interop.Common.Schema.Bson.JsonBsonConverter.TryConvertToBsonPrivate(String jsonDocument, BsonValue& bsonValue, Boolean retainSystemProperties, Boolean processTTLField) at Microsoft.Azure.Documents.Interop.Mongo.Common.BsonExtensions.ToMongoDBFormat(Document docDbDocument, Boolean enableBsonSchema, Boolean processTTLField, Boolean useLegacyUuidSerializationOrder) at Microsoft.Azure.Documents.Interop.Mongo.RequestHandlers.QueryHandler.<QueryAsync>d__0.MoveNext() --- End of stack trace from previous location where exception was thrown --- at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) at Microsoft.Azure.Documents.Interop.Mongo.MongoCommandProcessor.<QueryAsync>d__3.MoveNext() --- End of stack trace from previous location where exception was thrown ---
```

Provide customer with ready message below.

