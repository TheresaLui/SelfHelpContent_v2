<properties
	pageTitle="Check if failed to precreate account in ou"
	description="Check if failed to precreate account in ou"
	service=""
	resource=""
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="13cdb389-51ea-4390-bb32-dd2284d58e4e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if failed to connect to Azure SQL

HDInsight ESP cluster requires user assigned managed identity to precreate account in ou. A cluster can not be created if this creation fails. 

Use the Kusto command below to check SQL connections.

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "failed to precreate account in ou"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```