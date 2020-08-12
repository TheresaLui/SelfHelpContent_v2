<properties
	pageTitle="Check if failed to delete locked azure resource"
	description="Check if failed to delete locked azure resource"
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
	articleId="40810cff-7d0d-419b-97c8-5c5e443c8b7b"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if failed to delete locked azure resource

Run the below kusto query to check

```kusto
IaasClusterCRUDEvent
| where ClusterDnsName =~ ""{ClusterDnsName}"" and HdiDeploymentId =~ ""{HdiDeploymentId}"" and UserSubscriptionId =~ ""{UserSubscriptionId}""
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has ""AzureResourceLockedDeletionFailedErrorCode""
| project PreciseTimeStamp, State, ErrorInfoAsJson,InternalErrorMessage
```"

