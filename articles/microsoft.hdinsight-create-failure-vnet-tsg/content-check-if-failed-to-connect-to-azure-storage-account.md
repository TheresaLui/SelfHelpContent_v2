<properties
	pageTitle="Check if failed to connect to Azure Storage Account"
	description="Check if failed to connect to Azure Storage Account"
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
	articleId="bce1e0f1-f9cd-4238-9b50-60792f8544c6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if failed to connect to Azure Storage Account

A storage account is required for HDInsight. Use the command below to ensure that a connection to Azure Storage was made successfully. 

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "Failed to connect to Azure Storage Account"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```
