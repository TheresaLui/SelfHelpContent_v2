<properties
	pageTitle="usages telemetry"
	description="usages telemetry"
	infoBubbleText="usages telemetry"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="c4fd3b91-c47d-4604-bcfa-99d77778fe17"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747930"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
	
# Upload View And Usage Telemetry

Most users are able to resolve their "usage telemetry" related issue using the steps below, or a more detailed outline of the issue being experienced.

## **Recommended Steps**

To upload metrics for your Azure SQL managed instances to the Azure portal  follow these steps:

* Command to export logs locally. This will export all metrics to the specified file:

   ### Example:
   ```
   azdata arc dc export -t metrics --path metrics.json
   ```

* Upload metrics to Azure portal

   ### Example:
   ```
   azdata arc dc upload --path metrics.json
   ```
### Troubleshooting Steps

If you encounter issues you can use following troubleshooting techniques:

* Run azdata using the **--debug** switch
   ### Example: 
   ```
   azdata arc dc export -t metrics --path metrics.json --debug
   ```

* Examine the azdata.log for any errors or warnings and progress
   ### Example: 
   ```bash
   tail -n 300  ~/.azdata/logs/azdata.log
   ```

### Upload logs to Azure Monitor

This will export all logs to the specified file:

   ```bash
   azdata arc dc export -t logs -path logs.json
   ```
   This will upload logs to a Azure monitor log analytics workspace:

   ```bash
   azdata arc dc upload --path logs.json
   ```


### View the metrics in the Portal

Once your metrics are uploaded you should be able to visualize them from the Azure portal. To view your metrics in the portal, go to [Cost Management](https://ms.portal.azure.com/#blade/Microsoft_Azure_GTM/ModernBillingMenuBlade/Overview) blade on the Azure portal.

## **Recommended Documents**

- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [View Logs using Grafana & Kibana](https://docs.microsoft.com/azure/azure-arc/data/monitor-grafana-kibana)
- [Using PostgreSQL in Grafana](https://grafana.com/docs/grafana/latest/features/datasources/postgres/)
- [Create Azure Log Analytics Workspace](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace)
