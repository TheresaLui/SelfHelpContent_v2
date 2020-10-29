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
	articleId="6702938f-111d-4543-a916-d1a663e739d4"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if DNS is available

The hostname must resolve for HDInsight cluster creation to work successfully. Use the kusto command below to check if DNS is in use.

```kusto

IaasClusterCRUDEvent
| where ClusterDnsName =~ "{ClusterDnsName}" and HdiDeploymentId =~ "{HdiDeploymentId}" and UserSubscriptionId =~ "{UserSubscriptionId}"
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
| where ErrorInfoAsJson contains "DNS is available" and ErrorInfoAsJson contains "is not available" 
| project PreciseTimeStamp, State, ErrorInfoAsJson

```
