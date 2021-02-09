<properties
	pageTitle="Check if in DeleteError state"
	description="Check if in DeleteError state"
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
	articleId="5c7415e0-b6e1-4bc9-9315-724d533ab317"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if in DeleteError state

Review and validate the customer case:

1. UserSubscriptionId
2. ClusterDnsName
3. HdiDeploymentId
4. Issue time window

Run the below kusto query to get the error code with above information:

```kusto
IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}" 
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where State contains "Delete"
| project PreciseTimeStamp, State, ErrorInfoAsJson,InternalErrorMessage,RpRegionName,IsSecureHadoop,IsUserError,IsDeleteQueued
```

> **NOTE**: ***ErrorInfoAsJson*** and ***InternalErrorMessage*** is also important information to troubleshoot.
