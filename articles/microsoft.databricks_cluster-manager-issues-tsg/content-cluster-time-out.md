<properties
	pageTitle="Cluster Timeout Issue"
	description="Cluster Timeout Issue"
	service="Microsoft.Databricks"
	resource="Microsoft.Databricks/workspaces"
	ms.author="lahaddad"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="d804fc6b-09cf-4e4a-b79f-18a1e8eb479a"
   	ownershipId="AzureData_AzureDatabricks"
/>

# Cluster timeout issue

Cluster startup fails with error: *The Spark driver failed to start within 300 seconds.*

## Troubleshooting and Solution

1. Verify if customer is using external Metastore and Maven to download dependencies
2. Try to verify if cluster starts with internal Metastore
3. Verify customer is not blocking Outbound/Inbound connections to external repo's

Solution would be to store the Hive libraries in DBFS and access them locally from the DBFS location. We have [KB](https://docs.microsoft.com/en-us/azure/databricks/kb/clusters/cluster-failed-launch#cluster-timeout) for this as well.

If issue persists after trying the suggested approach, please discuss issue further with your SME/TA/EEE using [Ava](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312127/Ava), and [involve Databricks](https://supportability.visualstudio.com/AzureDataBricks/_wiki/wikis/AzureDataBricks.wiki/312121/Engaging-Databricks-Support) if needed.
