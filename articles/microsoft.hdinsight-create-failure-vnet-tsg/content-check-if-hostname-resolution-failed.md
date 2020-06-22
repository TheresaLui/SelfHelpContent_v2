<properties
	pageTitle="Check if HostName Resolution failed?"
	description="Check if HostName Resolution failed?"
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
	articleId="ef8d4db7-ae7f-47fc-a686-8ed2ba45b423"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if HostName Resolution failed?

Run the below kusto query to check


```sql

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson has "HostName Resolution failed"
| project PreciseTimeStamp, State, ErrorInfoAsJson

```
