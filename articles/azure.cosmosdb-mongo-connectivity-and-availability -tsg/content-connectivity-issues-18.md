<properties
	  pageTitle="Connectivity Issues"
	  description="Connectivity Issues"
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
	  articleId="45c51cd6-820b-42f0-8fa4-825521e2c92d"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Connectivity Issues

Please use this TSG for the following errors thrown by the MongoDB tools/drivers/

Closed connection [connectionId{localValue:<>, serverValue:<>}] to <>:10255 because there was a socket exception raised by this connection.
com.mongodb.MongoSocketWriteException: Exception sending message
 
##Getting the server connectionId from the client logs

With the v36 release, MongoDB service assigns a unique identifier to each connection and send this value to the client, which then logs it in its client log. This makes it very easy to correlate a client side connection with the server side connection.

- Ask the customer to enable connection logging for their driver based on the below references
- If logging was already enabled, get the driver logs from the customer and identify the connection that was faulty
 
e.g. The logs shared by the customer should have events as follows

``
2019-08-26 02:01:50,950] [INFO] [nioEventLoopGroup-2-1] [o.m.d.connection] [] : Closed connection [connectionId{localValue:837, serverValue:-1765686971}] to cdb-ms-prod-southcentralus1-fd2.documents.azure.com:10255 because there was a socket exception raised on another connection from this pool.

[2019-08-26 02:01:50,951] [ERROR] [nioEventLoopGroup-2-2] [o.s.b.a.w.r.e.AbstractErrorWebExceptionHandler] [traceId=e01ec6e6f9385537, spanId=a7c648df0693512d, spanExportable=false, X-Span-Export=false, X-B3-SpanId=a7c648df0693512d, X-B3-ParentSpanId=e01ec6e6f9385537, X-B3-TraceId=e01ec6e6f9385537, parentId=e01ec6e6f9385537] : [4671a61f] 500 Server Error for HTTP GET "/ws_infrastructure_rules/rules?tenant=jbhunt&eventType=CARRIER_RESTRICTIONS_TEST_V2"

org.springframework.data.mongodb.UncategorizedMongoDbException: Exception sending message; nested exception is com.mongodb.MongoSocketWriteException: Exception sending message
``

