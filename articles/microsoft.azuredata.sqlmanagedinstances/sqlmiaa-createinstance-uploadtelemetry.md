<properties
	pageTitle="SQL MIAA - Upload and view telemetry in Azure"
	description="SQL MIAA - Upload and view telemetry in Azure"
	infoBubbleText="SQL MIAA - Upload and view telemetry in Azure"
	service="microsoft.azuredata"
	resource="sqlmanagedinstances"
	ms.author="amigan,jopilov,prmadhes"
	displayOrder=""
	articleId="e6475182-b86c-46a8-870c-d042bafa11ca"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747941"
	resourceTags=""
	productPesIds="17125"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Managed_Instance_Azure_Arc"
/>

# Upload Metrics/Telemetry to Azure Portal

Most users are able to resolve their telemetry-related issue using the steps below.

## **Recommended Steps**

- **Upload Metrics to Azure Portal**

   To upload metrics for your Azure SQL managed instances, run the following CLI commands to export all metrics to the specified file:

   ```bash
   azdata arc dc export -t metrics --path metrics.json
   ```

   This will upload metrics to Azure monitor: 

   ```bash
   azdata arc dc upload --path metrics.json
   ```

- **View the metrics in the Portal**

   Once metrics are uploaded, you should be able to visualize them from the Azure portal.

## **Recommended Documents**

* [Upload resource inventory, usage data, metrics and logs to Azure Monitor](https://docs.microsoft.com/azure/azure-arc/data/upload-metrics-and-logs-to-azure-monitor)
