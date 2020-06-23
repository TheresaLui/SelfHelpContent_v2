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


Run the below kusto query to check


```sql

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "Failed to connect to Azure SQL"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```