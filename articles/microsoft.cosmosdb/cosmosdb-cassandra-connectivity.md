<properties
	pageTitle="Connectivity to Azure Cosmos DB Cassandra API"
	description="Troubleshoot Connectivity to Azure Cosmos DB Cassandra API"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32636776"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-cassandra-connectivity"
	displayOrder="141"
	category="Cassandra"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Unable to connect to Azure Cosmos DB Cassandra API 
Most users are able to resolve their Cassandra API connectivity issue using the steps below.


## **Recommended Steps**

### **Connectivity Issue**  
To resolve this issue, try one or more of the following methods:
* Ensure that the SSL is enabled in the connection options
* Check your firewall configuration for this service. Do you have Allow access from All networks or from Selected networks? If Selected networks is selected, do you have the IP address from which you are attempting to connect from added to the Allow list? Confirm that the list of approved IP addresses includes that of the client attempting to connect to your Cosmos DB Cassandra account.
* One way to test the connection is by accessing it from a location external to your network. This will allow you to rule out any network restrictions that may be causing the failure. One way to do this is by deploying an Azure virtual machine and running your application from the Azure VM to eliminate any network restrictions.  

### **Timeout Issue while using the Cassandra API Tutorial**  
* Properly convert the .crt to .cer file [cosmos_sample.js](https://gist.github.com/prashanthmadi/afba93b4871fd8e79f22e13ecf05ecfc)
* Do not deactivate the TLS
* Verify the Node.js version you are using


### **Connection Timeout Error**  
Verify the code is setting a connectTimeout

```
var ssl_option = {
    cert: fs.readFile('E:\\Tools\\certs\\bc2025.cer'),
    rejectUnauthorized: true,
    secureProtocol: 'TLSv1_2_method',
    checkServerIdentity: () => { return null; },
};

var socket_Options = {
    connectTimeout: 15000
};

const authProviderLocalCassandra = new cassandra.auth.PlainTextAuthProvider('USERNAME', 'KEY==');
const client = new cassandra.Client({ contactPoints: ['USERNAME.cassandra.cosmos.azure.com:10350'], authProvider: authProviderLocalCassandra, sslOptions: ssl_option, socketOptions: socket_Options });
```   



## **Recommended Documents**

[Quickstart: Build a Cassandra app with .NET SDK and Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-dotnet)
<br>This quickstart shows how to use .NET and the Azure Cosmos DB Cassandra API to build a profile app by cloning an example from GitHub.  

[Quickstart: Build a Java app to manage Azure Cosmos DB Cassandra API data](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-java)
<br>This quickstart shows how to use Java and the Azure Cosmos DB Cassandra API to build a profile app by cloning an example from GitHub.  

[Quickstart: Build a Cassandra app with Node.js SDK and Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-nodejs)
<br>This quickstart shows how to use Node.js and the Azure Cosmos DB Cassandra API to build a profile app by cloning an example from GitHub.  

[Quickstart: Build a Cassandra app with Python SDK and Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/create-cassandra-python)
<br>This quickstart shows how to use Python and the Azure Cosmos DB Cassandra API to build a profile app by cloning an example from GitHub.