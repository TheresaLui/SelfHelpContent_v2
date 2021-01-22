<properties
	pageTitle="Monitor Cosmos with DB How-to"
	description="Configure Cosmos DB How-to"
	service="microsoft.documentdb"
	resource="databaseAccounts"
	authors="jimsch"
	ms.author="jimsch"
	selfHelpType="generic"
	supportTopicIds="32783704"
	resourceTags=""
	productPesIds="15585"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="cosmosdb-monitoring-howto"
	displayOrder="261"
	category="Monitoring"
	ownershipId="AzureData_AzureCosmosDB"
/>

# Monitor Cosmos DB Monitoring How-to 

Most users are able to resolve their Monitoring Alert issue following the recommended steps and reading the recommended documents provided below.  


## **Recommended Steps**  

### **Setting up an Alert for RU consumption**  
Please note that you can monitor the RU consumption from Azure portal.  You can do this by navigating to your Cosmos DB account, open the alerts blade and you can setup metric or activity log alerts to send you notifications if the consumption has reached a certain limit.  


### **You received an alert with your monitor**  
If you receive an alert from your monitor:
1.  Determine what the alert is regarding and your account type, then navigate back in your browser to where you began your Support Request flow at *Let us begin by understanding more about your issue by selecting a Problem type*
2.  Change the Problem type from *Monitoring Alerts* to a more relevant type that will provide you targeted recommendations of how to address this specific alert.  For example if you received an *exceeding throughput* alert, you may want to change your problem type to *Throughput and Scaling*, or if your account is a MongoDB account, then choosing a problem type relevant to MongoDB might provide you the self help solution you need.  


## **Recommended Documents**  

[Create, view, and manage alerts using Azure Monitor](https://docs.microsoft.com/azure/monitoring-and-diagnostics/monitor-alerts-unified-usage)
<br>Metric alerts in Azure Monitor provide a way to get notified when one of your metrics cross a threshold. Metric alerts work on a range of multi-dimensional platform metrics, custom metrics, Application Insights standard and custom metrics. In this article, we will describe how to create, view and manage metric alert rules through Azure portal and Azure CLI.  

[Monitor Azure Cosmos DB data by using diagnostic settings in Azure](https://docs.microsoft.com/azure/cosmos-db/cosmosdb-monitor-resource-logs)
<br>Diagnostic settings in Azure are used to collect resource logs. This article provides troubleshooting and the properties emitted.   

[Monitoring and debugging with metrics in Azure Cosmos DB](https://docs.microsoft.com/azure/cosmos-db/use-metrics)
<br>Azure Cosmos DB provides metrics for throughput, storage, consistency, availability, and latency. The Azure portal provides an aggregated view of these metrics. You can also view Azure Cosmos DB metrics from Azure Monitor API.  

[Monitor Cosmos DB with alerts](https://docs.microsoft.com/azure/cosmos-db/monitor-accounts)
<br>You can monitor your Azure Cosmos DB accounts in the Azure portal. For each Azure Cosmos DB account, a full suite of metrics is available to monitor throughput, storage, availability, latency, and consistency. Metrics can be reviewed on the Account page, the new Metrics page, or in Azure Monitor.  

[Understand how metric alerts work in Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric-overview)
<br>This article describes how you can define a metric alert rule by specifying a target resource to be monitored, metric name, condition type (static or dynamic), and the condition (an operator and a threshold/sensitivity) and an action group to be triggered when the alert rule fires. Condition types affect the way thresholds are determined. 

