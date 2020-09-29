<properties
	pageTitle="Check if failed to connect to AD"
	description="Check if failed to connect to AD"
            service="Microsoft.HDInsight"
            resource="Microsoft.HDInsight/clusters"
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="90356749-dfc7-4717-8679-8030a16d64af"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if failed to connect to Azure Storage Account

AADDS is required for HDInsight ESP cluster. Use the below kusto query to ensure that a connection to AD was made successfully. 

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "failed to connect to AD"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```
