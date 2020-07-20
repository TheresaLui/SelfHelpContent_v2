<properties
	pageTitle="How to check CRUD error code"
	description="How to check CRUD error code"
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
	articleId="e5042cad-19bd-43b5-a841-971254d5e822"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# How to check CRUD error code

Review and validate customer case:
1. UserSubscriptionId
2. ClusterDnsName
3. HdiDeploymentId
4. Issue time window

Run the below kusto query to get the error code with above information

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}" 
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| extend d=parse_json(ErrorInfoAsJson)
| project PreciseTimeStamp, State, ErrorInfoAsJson,d[0]["ErrorCode"]

```
