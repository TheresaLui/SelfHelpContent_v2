<properties
    pageTitle="Cassandra Timeout RCA"
    description="RCA - Cassandra Timeout"
    infoBubbleText="We are aware of an issue in our service that might result in operation timeout errors in your Cassandra application for idle connections. See the details on the right."
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="andresferreira"
    ms.author="anferrei"
    articleId="cosmosdb-cassandra-timeout-rca"
    diagnosticScenario="CosmosDBCassandraTimeoutInsight"
    selfHelpType="rca"
    supportTopicIds="32636776"
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# Cassandra Timeout

## We ran diagnostics on your account **<!--$GlobalDatabaseAccountName-->[GlobalDatabaseAccountName]<!--/$GlobalDatabaseAccountName-->** and found an issue

<!--issueDescription-->
We are aware of an issue in our service that might result in operation timeout errors in your Cassandra application for idle connections. These errors are safe to ignore until we fix the issue.
<!--/issueDescription-->

## **Recommended Steps**

Some of the Cassandra drivers may handle these timeout errors automatically but some drivers may not.
You want to change your application code to re-connect to our service when you get operation timeouts on idle connections. This can be done by catching specific operation timeout error and re-connecting before retrying the same operation.

If you’re making use of a development framework (such as spring boot for Java, or similar) with auto configuration and you are facing this issue, you may need to manually create connections, rather than leveraging any auto wiring, so that you can explicitly re-create connections in code, in case of **OperationTimeout exception**.

In case you are using Java SDK(V3 drivers) use the library mentined inthe [Azure Cosmos Cassandra Extensions for Java](https://github.com/Azure/azure-cosmos-cassandra-extensions) to fix the issue.
