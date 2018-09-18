<properties
	pageTitle="Request Timeout"
	description="Request Timeout"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="balaksms"
	displayOrder="85"
	selfHelpType="resource"
	supportTopicIds="32597555"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# Bulk Delete operation fails with request timeouts

You are getting a request timeout exception when calling a server side procedure which deletes documents in a loop.  The best practice is to batch the delete using some top 100 or 1000 document by checking the deleted count and return the response to the
client. The client application can then call the procedure again in a loop to complete the deletion of documents.

Example:
if(responseBody.deleted <1000)
                {   
                    console.log("Call to trydelete")
                    tryDelete(documents);
                }
                else
                {
                    console.log("Call to Response")
                    response.setBody(responseBody);    
                }



The above method would avoid the timeout and ensure all the documents are deleted.

Please contact support if you are getting timeout other than the above scenario


## **Recommended documents**

* [Performance tips for Azure Cosmos DB and .NET](https://docs.microsoft.com/azure/cosmos-db/performance-tips)

* [Performance tips for Azure Cosmos DB and Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-java)

* [Performance tips for Azure Cosmos DB and Async Java](https://docs.microsoft.com/azure/cosmos-db/performance-tips-async-java)
