<properties
	pageTitle="How to check CRUD error code"
	description="How to check CRUD error code"
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
	articleId="fc5e8202-7ad7-4077-abed-c99a25099ea7"
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
