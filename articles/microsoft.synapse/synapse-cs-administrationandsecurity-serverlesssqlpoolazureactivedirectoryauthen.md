<properties
    selfHelpType = "generic"
    cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId = "AzureData_SynapseAnalytics"
    service = "microsoft.synapse"
    resource = "workspaces"
    resourceTags = ""
    productPesIds = "15818"
    supportTopicIds = "32783904"
    displayOrder = ""
    diagnosticScenario = ""
    infoBubbleText = ""
    pageTitle = "Administration and Security/Serverless SQL pool - Azure Active Directory Authentication"
    description = "Administration and Security/Serverless SQL pool - Azure Active Directory Authentication"
    articleId = "synapse-cs-administrationandsecurity-serverlesssqlpoolazureactivedirectoryauthen.md"
    ms.author = "fipopovi, saltug"
/>

# Administration and Security/Serverless SQL pool - Azure Active Directory Authentication

## **Recommended Steps**

* Check if you have permissions to log into Serverless SQL pool. To gain access, one of the Azure Synapse workspace administrators should add you to workspace administrator or SQL administrator role. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control). 

* Make sure you are connecting to database you are given access to. To connect to specific database using SSMS, check [Connect to Server (Connection Properties Page)](https://docs.microsoft.com/sql/ssms/f1-help/connect-to-server-connection-properties-page-database-engine?view=sql-server-ver15). For ADS, check [Use Azure Data Studio to connect and query](https://docs.microsoft.com/sql/azure-data-studio/quickstart-sql-database?view=sql-server-ver15). 

* If using Synapse Studio, your network might prevent communication to Azure Synapse backend. Most frequent case is that port 1443 is blocked. To get the Serverless SQL pool to work unblock this port. Other problems could prevent Serverless SQL pool to work as well, [visit full troubleshooting guide for more information](https://docs.microsoft.com/azure/synapse-analytics/troubleshoot/troubleshoot-synapse-studio). 

* If using SSMS or ADS, check if your network blocks port 1433. 

* If using ADF to access Serverless SQL pool, check if MSI account for your workspace is given permission to log in. [Visit full guide on access control for more information](https://docs.microsoft.com/azure/synapse-analytics/sql/access-control) 

 