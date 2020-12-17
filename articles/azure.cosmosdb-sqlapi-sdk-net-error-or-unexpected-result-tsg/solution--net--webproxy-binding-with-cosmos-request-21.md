<properties
	  pageTitle=".Net: WebProxy Binding with Cosmos request"
	  description=".Net: WebProxy Binding with Cosmos request"
      service="Microsoft.DocumentDB"
      resource="databaseAccounts"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="7652165f-6f5b-4712-bc52-82ff08957aab"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# .Net: WebProxy Binding with Cosmos request

<!--issueDescription-->

Dear customer,

If you Customer are facing issue while connecting to Cosmos DB using a WebProxy instance. Please confirm create a handler of the proxy object and then pass the handler object to the DocumentDB client constructor

```
HttpClientHandler handler = new HttpClientHandler()
    {
        Proxy = proxyObject
        UseProxy = true,
    };
DocumentClient client = new DocumentClient(new Uri("yourEndpoint"), "yourKey", handler);
```

Thank you.

<!--/issueDescription-->

