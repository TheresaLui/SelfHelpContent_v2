<properties
	pageTitle="Check if DNS is available"
	description="Check if DNS is available"
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
	articleId="2f8ebc4e-f3ec-409f-b128-7030f76b2845"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if DNS is available

The hostname must resolve for HDInsight cluster creation to work successfully. Use the following `kusto` command to check if DNS is in use:

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson contains "DNS is available" and ErrorInfoAsJson contains "is not available" 
| project PreciseTimeStamp, State, ErrorInfoAsJson
```
