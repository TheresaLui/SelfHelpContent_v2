<properties
	pageTitle="Databricks Logging Issues"
	description="Databricks Logging Issues"
	service="microsoft.Databricks"
	resource="workspaces"
	authors="kywe665"
	displayOrder="8"
	selfHelpType="resource"
	supportTopicIds="32612200"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="1e7343d1-bda8-4872-86ba-622ea3c1f0e7"
	ownershipId="AzureData_AzureDatabricks"
/> 

# Azure Databricks Logging

## **Recommended steps**

- You can [find Driver logs](https://docs.databricks.com/spark/latest/rdd-streaming/debugging-streaming-applications.html#driver-logs) for exception stack traces and DStream DAG prints
- You can find [Event logs](https://docs.databricks.com/user-guide/clusters/event-log.html#event-log) in the cluster settings page to understand cluster lifecycle events
- You can find [Executor logs](https://docs.databricks.com/spark/latest/rdd-streaming/debugging-streaming-applications.html#executor-logs) in the Spark UI to help diagnose why a certain task may be misbehaving

## **Recommended documents**

1. If you need more verbose logging [following these instructions](https://docs.azuredatabricks.net/user-guide/clusters/tips/set-executor-log-level.html)
2. To find where your logs are saved after cluster termination, [check the cluster log path](https://docs.databricks.com/user-guide/clusters/log-delivery.html)
