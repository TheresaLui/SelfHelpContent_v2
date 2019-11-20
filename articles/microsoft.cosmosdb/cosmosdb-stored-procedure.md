<properties
	pageTitle="Stored procedure programming"
	description="Stored Procedure programming"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="mkolt"
	ms.author="mkolt"
	selfHelpType="resource"
	supportTopicIds="32636829"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public"
	articleId="cosmosdb-stored-procedure"
	displayOrder="66"
	category="Core (SQL)"
/>

# Troubleshooting stored procedures

## **Recommended Steps**

### **General Guidelines**

* Stored procedures are recommended for scenarios that need bulk operations or for scenarios that require transactions. Besides, stored procedures are recommended for write operations. You may run into RU bottlenecks if you use stored procedures for read-only operations.
  * Ideally, stored procedure should do maximum write operations and minimal read and compute operations.
* Each stored procedure request runs within transaction scope.
  * All or none rule: if stored procedure request modifies multiple documents, they all either get committed or all get reverted.
  * If two stored procedure requests modify same document, one will succeed and the other one will fail with 449 (RetryWith). SDK retries on 449 by default.
  * If an exception is thrown and is not handled by stored procedure, it will abort the transaction.
* Each stored procedure request is scoped to a single partition key specified via [Partition Key RequestOption in .NET](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.requestoptions.partitionkey?view=azure-dotnet) or [Partition Key RequestOption in Java](https://docs.microsoft.com/java/api/com.microsoft.azure.documentdb.requestoptions.setpartitionkey?view=azure-java-stable#com_microsoft_azure_documentdb_RequestOptions_setPartitionKey_PartitionKey_). Queries within a stored procedure are also automatically scoped to the same partition key value.
* Each stored procedure request runs in a sandbox:
  * Timeout of [5 seconds](https://docs.microsoft.com/azure/cosmos-db/concepts-limits).
  * RU limit: 
    * [2 seconds] of primary replica time in RU units. Example: if the collection has 2 partitions and 10,000 RU/s throughput for the entire collection, that would be 2 (seconds) * 10,000 (RU/s) / 2 (partitions) / 4 (replicas per partition) = 2,500 RU.
    * The replica rate limiter uses RU cost specific only to this replica, with write cost being lower than one reported to the client, in particular for of 1kb document the cost of a read is ~1 RU and create cost is ~1.25 RU. The RU cost for writes done from script reported to the client accommodates for replication on 3 secondary replicas, that is why the cost of one create becomes ~5 RU.
    * Total script request cost consists of read RUs, write RUs and compute-only RUs, the latter is computed based on actual CPU cycles consumed.
* Stored procedures return Status Code = 400 (Bad Request) on any failure.
   * HTTP Status Code for exceptions originated from CRUD execution, such as NotFound (404), would be in `Error.number` of the exception and will get to client as Substatus Code of stored procedure request.
   * You can also throw custom exception using `Error.number`: throw new Error(1234, "error message"). The first argument must be 2 byte integer and would get into Substatus Code of stored procedure request.
   * You can examine the Substatus Code by using the `x-ms-substatus` response header. Refer to [Example (C#)](https://github.com/Azure/azure-documentdb-changefeedprocessor-dotnet/blob/master/src/DocumentDB.ChangeFeedProcessor/DocDBErrors/SubStatusHelpers.cs) on how to obtain header value from DocumentClientException.
* Best practices using stored procedures to avoid running into timeouts (HTTP Status Code = 408) and RU consumption violations:
  * The return value (`isAccepted`) of each CRUD or Query call from within stored procedure, must be checked. See [Stored procedure sample using IsAccepted](https://github.com/Azure/azure-cosmos-dotnet-v2/blob/fd036405a7de6b8bc4c9fdbc6872b09f9b6e2bf3/samples/code-samples/ServerSideScripts/JS/BulkImport.js#L50-L58) for a sample that breaks up and resumes execution using this pattern.
  * All CRUD calls in stored procedures must be serialized in the sense the each next CRUD call must be done from previous CRUD callback.
  * Simplest way to achieve this serialization is to use `async await` wrapper (see example below) and throw  when `isAccepted` is false.
  * Each CRUD call is asynchronous, and after a call is made, all further processing depending on the result of the call should be done from the callback.
  * Avoid infinite loops and excessive CPU consumption in between CRUD calls.
* You can debug stored procedures locally using the [Cosmos DB Emulator](https://docs.microsoft.com/azure/cosmos-db/local-emulator) or by adding `console.log()` statements and enabling [Enable Script Logging RequestOption in .NET](https://docs.microsoft.com/dotnet/api/microsoft.azure.documents.client.requestoptions.enablescriptlogging?view=azure-dotnet) or [Enable Script Logging RequestOption in Java](https://docs.microsoft.com/java/api/com.microsoft.azure.documentdb.requestoptions.setscriptloggingenabled?view=azure-java-stable#com_microsoft_azure_documentdb_RequestOptions_setScriptLoggingEnabled_boolean_) via RequestOptions.
  * The limit for log size created by console.log() is 8KB.

### **Frequently Asked Questions**

* Which JavaScript version is used to run server-side scripts?
  It is ES6 with support for ES7 `async await` feature.
* Is it possible to use `async await` JavaScript feature?

  Yes. Note that current Server-side scripting API is callback based but it is possible to write a small async wrapper on top of current API and use it with async await. Using `await` makes source code much simpler and easier to write. The example below demonstrates how to do that:
```javascript
	function async_sample(continuation) {
		const ERROR_CODE = { NotAccepted: 429 };

		const asyncHelper = {
			queryDocuments(sqlQuery, options) {
				return new Promise((resolve, reject) => {
					const isAccepted = __.queryDocuments(__.getSelfLink(), sqlQuery, options, (err, feed, options) => {
						if (err) reject(err);
						resolve({ feed, options });
					});
					if (!isAccepted) reject(new Error(ERROR_CODE.NotAccepted, "queryDocuments was not accepted."));
				});
			},

			replaceDocument(doc) {
				return new Promise((resolve, reject) => {
					const isAccepted = __.replaceDocument(doc._self, doc, (err, result, options) => {
						if (err) reject(err);
						resolve({ result, options });
					});
					if (!isAccepted) reject(new Error(ERROR_CODE.NotAccepted, "replaceDocument was not accepted."));
				});
			}
		};

		async function main() {
			let count = 0;
			try {
				do {
					let { feed, options } = await asyncHelper.queryDocuments("SELECT * from c", { continuation });

					for (let doc of feed) {
						doc.newProp = "new value";
						await asyncHelper.replaceDocument(doc);
						++count;
					}

					continuation = options.continuation;
				} while (continuation);

				__.response.setBody({ count });
			} catch (err) {
				if (err.Number === 429) {
					// Handle preemption, typically just return continuation to the client.
					__.response.setBody({ count, continuation });
				}
				else throw err;
			}
		}

		main().catch(err => getContext().abort(err));
	}
```
* When using promises, how to abort script transaction?
  Use `getContext().abort()` API like this:
  ```javascript
  getContext().abort(new Error("my exception"));
  ```
* How to use console.log?

  See above, **General Guidelines** section.
* How to retrieve HTTP Status Code from CRUD on the client side?

  See above, **General Guidelines** section, note about `x-ms-substatus`.
* How to communicate error code back to the client?

  See above, **General Guidelines** section, note about `x-ms-substatus`.

### **Troubleshooting Steps**

The information below is targeted toward specific issues.

* A query run from stored procedure does not find any documents
  * Make sure that partition key value is passed correctly when creating stored procedure  request from the client. Pass partition key value (such as "Seattle") and not the name of field used as part of partition key definition (such as /city).
  * Make sure that continuation is drained. There are no documents matching a query if and only if the query returns no results and response continuation token is empty.
  * When indexing policy is used, a query run from within script will not see updates done by current script execution. The index is updated during commit time.
  * Make sure that indexing of collection is not in progress in case indexing policy was recently changed.
* A script was disabled for execution
  * Review script source code and make sure it follows the guidelines.
  * See "using stored procedures to avoid running into timeouts" under **Best Practices** section.
* Script times out
  * See "using stored procedures to avoid running into timeouts" under **Best Practices** section.
  * For bulk operations, as workaround, consider lowering the number of CRUD calls from script.
* If none of this matches the issue, continue creating an incident and make sure to provide the following information:
  * Subscription Id.
  * Document Service Id.
  * Region.
  * Database and collection name.
  * Script resource name.
  * Activity Id.
  * Approximate timestamp (include time zone).
  * Full exception information on the client side (if applicable).
  * Script source code.

## **Recommended Documents**

* [Cosmos DB Server-side JavaScript API](https://azure.github.io/azure-cosmosdb-js-server/)<br/>
This contains reference documentation for server-side scripting API.
* [Azure Cosmos DB server-side programming: Stored procedures, database triggers, and UDFs](https://docs.microsoft.com/azure/cosmos-db/stored-procedures-triggers-udfs)<br/>
Azure Cosmos DB provides language-integrated, transactional execution of JavaScript. When using the SQL API in Azure Cosmos DB, you can write stored procedures, triggers, and user-defined functions (UDFs) in the JavaScript language. You can write your logic in JavaScript that executed inside the database engine. You can create and execute triggers, stored procedures, and UDFs by using Azure portal, the JavaScript language integrated query API in Azure Cosmos DB or the Cosmos DB SQL API client SDKs.
* [Server-side script samples](https://github.com/Azure/azure-cosmos-dotnet-v2/tree/fd036405a7de6b8bc4c9fdbc6872b09f9b6e2bf3/samples/code-samples/ServerSideScripts)<br/>
This contains a variety of sample code snippets and applications built using Azure Cosmos DB and the .NET SDK and server-side scripts written in JavaScript. These samples demonstrate how to use the .NET Client SDK to interact with stored procedures, triggers, and user-defined functions that run on the server-side in the Azure Cosmos DB service.
