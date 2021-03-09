<properties
	pageTitle="Escalation"
	description="Escalation"
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
	articleId="5ddf09a2-e705-430f-92f4-d3f64eea3ad2"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Escalation

<!--issueDescription-->
**INTERNAL CONTENT! DO NOT PROVIDE TO CUSTOMER!**
<!--/issueDescription-->

1. Try to run below kql to check RCA
```
LogEntry
| where ClusterDnsNamecontains "{ClusterDnsName}" 
| order by PreciseTimeStamp desc 
| where TraceLevel != "Verbose"
| where Details contains "Deletion" or Details contains "delete"
| project PreciseTimeStamp,TraceLevel, UserSubscriptionId, Class, Details
| where PreciseTimeStamp > datetime('{yyyy-mm-dd HH:MI:SS}') and PreciseTimeStamp < datetime('{yyyy-mm-dd HH:MI:SS}')
```
2. Try to follow the recommended documents to delete DeleteError cluster or escalate:

## **Recommended Documents**

* [DeleteError](https://supportability.visualstudio.com/AzureHDinsight/_wiki/wikis/AzureHDinsight/349535/Cluster-deletion-failure-DeleteError)
