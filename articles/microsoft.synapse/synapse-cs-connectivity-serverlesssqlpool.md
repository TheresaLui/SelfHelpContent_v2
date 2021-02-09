<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783902"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Connectivity/Serverless SQL pool"
    description = "Connectivity/Serverless SQL pool"
    articleId = "synapse-cs-connectivity-serverlesssqlpool.md"
    ms.author = "fipopovi,saltug,goventur"
/>

# Connectivity/Serverless SQL pool

## **Recommended Steps**

* Check if you have permissions to log in to Serverless SQL pool. To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control). 

* Make sure you are connecting to database that you are given access to. To connect to specific database using SSMS, check [Connect to Server (Connection Properties Page)](https://docs.microsoft.com/sql/ssms/f1-help/connect-to-server-connection-properties-page-database-engine?view=sql-server-ver15). For ADS, check [Use Azure Data Studio to connect and query](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-database?view=sql-server-ver15). 

* To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control). 

* If using Synapse Studio, check if your network blocks port 1443 and unblock it. 

* If using SSMS or ADS, check if your network blocks port 1433 and unblock it.

* If using SSMS or ADS and you notice an issue with object explorer, update SSMS and ADS to the latest version.

 