<properties
	  pageTitle="Ask Customer to enable logging"
	  description="Ask Customer to enable logging"
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
	  articleId="1764fac7-db77-4462-b734-8f47c5f4adeb"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Ask Customer to enable logging

<!--issueDescription-->

Dear customer,

Please kindly enable the connection logging for your drived based on the below reference.

e.g. The logs shared by you should have events as follows

``
2019-08-26 02:01:50,950] [INFO] [nioEventLoopGroup-2-1] [o.m.d.connection] [] : Closed connection [connectionId{localValue:837, serverValue:-1765686971}] to cdb-ms-prod-southcentralus1-fd2.documents.azure.com:10255 because there was a socket exception raised on another connection from this pool.

[2019-08-26 02:01:50,951] [ERROR] [nioEventLoopGroup-2-2] [o.s.b.a.w.r.e.AbstractErrorWebExceptionHandler] [traceId=e01ec6e6f9385537, spanId=a7c648df0693512d, spanExportable=false, X-Span-Export=false, X-B3-SpanId=a7c648df0693512d, X-B3-ParentSpanId=e01ec6e6f9385537, X-B3-TraceId=e01ec6e6f9385537, parentId=e01ec6e6f9385537] : [4671a61f] 500 Server Error for HTTP GET "/ws_infrastructure_rules/rules?tenant=jbhunt&eventType=CARRIER_RESTRICTIONS_TEST_V2"

org.springframework.data.mongodb.UncategorizedMongoDbException: Exception sending message; nested exception is com.mongodb.MongoSocketWriteException: Exception sending message
``

Thank you.

<!--/issueDescription-->

