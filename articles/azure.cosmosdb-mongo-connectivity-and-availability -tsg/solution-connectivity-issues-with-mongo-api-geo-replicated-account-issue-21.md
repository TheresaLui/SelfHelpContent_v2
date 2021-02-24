<properties
	  pageTitle="Connectivity Issues with Mongo API Geo-Replicated account issue"
	  description="Connectivity Issues with Mongo API Geo-Replicated account issue"
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
	  articleId="b6ead22f-372c-4d9a-88a1-751e1acbc8bb"
	  ownershipId="AzureData_AzureCosmosDB"
/>

# Connectivity Issues with Mongo API Geo-Replicated account issue

<!--issueDescription-->
### ** THIS IS NOT A CUSTOMER READY CONTENT MESSAGE **

**Next steps:** 
All mongo C# client and Java drivers does not work seamlessly with Cosmos DB Mongo API account with Geo-Replication. We need to use specific connection string along with specific driver versions.

For mongo 3.2 account, the C# driver version < 2.8.0 ( Java driver version < 3.8.0 ) will not issue requests to read regions. For 3.6 mongo accounts, including the appName in the connection string (as provided in the portal) is required for drivers of any version to issue requests to read regions.

Advice to customers with multi-region accounts on 3.2 is to use a driver < 2.8 if they want to issue requests to their read region. For 3.6 accounts, advice is to use the latest driver and always include appName.

#### Customer Impact
This prevents the customer from being able to utilize geo replication features of Cosmos DB Mongo API from C# and Java driver.

####Symptoms
Customer is not able to connect to different regions (or not able to connect at all) to a mulit-region account.

<br>

#### Solution
Please see [PG TSG 1204: Working with C# driver and Mongo API Geo-Replicated account](https://cosmosdbdocs.azurewebsites.net/tsg/tsg1204.html)

Please see [PG TSG 1205: Working with C# driver and Mongo API Multimaster account](https://cosmosdbdocs.azurewebsites.net/tsg/tsg1205.html)


##More Information
Sometimes Java dependencies may load two versions of the same library. To make application use the proper driver version with 3.2 endpoint, a change in the order of dependencies was required in the pom.xml file (reference case: 120093024006390).

The dependency below will use 3.7.1 version, but a pom.xml file with springboot dependency listed first will use a different driver version (loaded by a nested dependency).

```
<dependency>
	<groupId>org.mongodb</groupId>
	<artifactId>mongo-java-driver</artifactId>
	<version>3.7.1</version>
</dependency>
<dependency>
	<groupId>org.springframework.boot</groupId>
	<artifactId>spring-boot-starter-data-mongodb</artifactId>
</dependency>
```

## Customer message:
Based on the troubleshooting step before, please write your conclusions to customer. Don't include any Kusto Query.

<!--/issueDescription-->

