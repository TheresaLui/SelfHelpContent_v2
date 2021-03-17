<properties
	pageTitle="How to check Scale error code"
	description="How to check Scale error code"
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
	articleId="f132b97b-eb53-4d67-84d5-e252452fde8a"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check Scale error code

Review and validate customer case:
1. UserSubscriptionId
2. ClusterDnsName
3. HdiDeploymentId
4. Issue time window

Run the below kusto query to get the error code with above information

```kusto

IaasClusterScaleEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}" 
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| extend d=parse_json(ErrorInfoAsJson)
| project PreciseTimeStamp,State,ScaleOperation,ScaleFrom,RequestedScaleTo,ScaledTo,IsAutoscale,IsUserError,ErrorInfoAsJson,ScalingInternalErrorMessage,d[0]["ErrorCode"]

```

> **NOTE**: ***ErrorInfoAsJson*** and ***ScalingInternalErrorMessage*** are also important information to troubleshoot
