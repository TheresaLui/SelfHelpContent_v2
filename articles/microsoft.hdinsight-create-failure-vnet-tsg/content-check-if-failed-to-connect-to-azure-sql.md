<properties
	pageTitle="Check if failed to connect to Azure SQL"
	description="Check if failed to connect to Azure SQL"
	service=""
	resource=""
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="06db9291-6c96-47c0-96a4-df7a339142e2"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if failed to connect to Azure SQL

HDInsight requires a connection to a SQL server as a main function of HDInsight. A cluster can not be created if this connection to SQL fails. 

Use the Kusto command below to check SQL connections.

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "Failed to connect to Azure SQL"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```