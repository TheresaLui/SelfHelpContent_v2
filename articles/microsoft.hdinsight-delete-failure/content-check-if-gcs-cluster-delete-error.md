<properties
	pageTitle="Check if GCS cluster delete error"
	description="Check if GCS cluster delete error"
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
	articleId="04f2c0f9-72d9-454d-9047-b0a53e6d032e"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if GCS cluster delete error

## **Recommended Steps**

Review and validate customer case:

1. UserSubscriptionId
2. ClusterDnsName
3. HdiDeploymentId
4. Issue time window

Run the below kusto query to get the error code with above information:

```sql
IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}" 
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "AzureResourceDeletionFailedErrorCode" and InternalErrorMessage  has "trying to delete certificate from KeyVault"
| project PreciseTimeStamp, State, ErrorInfoAsJson,InternalErrorMessage
```
