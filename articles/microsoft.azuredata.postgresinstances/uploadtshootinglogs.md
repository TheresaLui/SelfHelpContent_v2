<properties
	pageTitle="View Upload logs telemetry"
	description="View Upload logs telemetry"
	infoBubbleText="View Upload logs telemetry"
	service="microsoft.azuredata"
	resource="postgresinstances"
	ms.author="pookam"
	displayOrder=""
	articleId="7c708b03-ba2a-4fb3-b576-5d4c0616aa10"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32747929"
	resourceTags=""
	productPesIds="17124"
	cloudEnvironments="Public, fairfax, usnat, ussec"
	ownershipId="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale"
    />
	
# Upload Logs and view Telemetry

With Azure Arc data services you can optionally upload your metrics and logs to Azure Monitor so you can aggregate and analyze metrics, logs, raise alerts, send notifications or trigger automated actions. Sending your data to Azure Monitor also allows you to store monitoring and logs data off site and at huge scale enabling long-term storage of the data for advanced analytics.
Most users are able to resolve their issues with resources view related telemetry for a PostgreSQL Hyperscale Server Group on Azure Arc using the recommended documents below.

## **Recommended Steps**

* Before you begin ensure you have followed the one time steps
  * Create a service principal/Azure Active Directory application including creating a client access secret and assign the service principal to the 'Monitoring Metrics Publisher' role on the subscription(s) where your database instance resources are located
    * Creating a service principal requires certain [permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal)in Azure. You may need to contact your Azure Administrator for the same.
  * Create a log analytics workspace and get the keys and set the information in environment variables
  * The first item is required to upload metrics and the second one is required to upload logs
  * You will need to assign it the 'Monitoring Metrics Publisher' and 'Contributor' roles so that the service principal can upload metrics and perform create and upload operation
  * You can find the commands to follow the pre-requisites [here](https://docs.microsoft.com/azure/azure-arc/data/upload-metrics-and-logs-to-azure-monitor#before-you-begin)
* Once you have completed the pre-requisites you continue to follow the below steps to upload logs to Azure Monitor

### Upload Logs to Azure Monitor

This will export all relevant logs from PostgreSQL server group on Arc to the specified file:

   ```bash
   azdata arc dc export -t logs -path logs.json
   ```

This will upload logs to a Azure monitor log analytics workspace:

   ```bash
   azdata arc dc upload --path logs.json

   ```

## View your logs in Azure Portal

Once your logs are uploaded, you should be able to query them using the log query explorer as follows:

* Open the Azure Portal and then search for your workspace by name in the search  bar at the top and then select it
* Click Logs in the left panel
* Click Get Started (or click the links on the Getting Started page) to learn more about Log Analytics if you are new to it)
* Follow the tutorial to learn more about Log Analytics if is is your first time using the technology
* Expand Custom Logs at the bottom of the list of tables and you will see a table called 'sql_instance_logs_CL'
* Click the 'eye' icon next to the table name
* Click the 'View in query editor' button
* You'll now have a query in the query editor which will show the most recent 10 events in the log
* From here, you can experiment with querying the logs using the query editor, set alerts, etc

### Troubleshooting Steps

If you have any failures, you can view the azdata log by issuing a command like this.

   ```bash
   cat azdata.log |grep -v "DEBUG"| tail -n 500
   ```
   
## **Recommended Documents**   

- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)
- [Getting logs for Azure Arc enabled data services](https://docs.microsoft.com/azure/azure-arc/data/troubleshooting-get-logs)
- [View Logs using Grafana & Kibana](https://docs.microsoft.com/azure/azure-arc/data/monitor-grafana-kibana)
- [Using PostgreSQL in Grafana](https://grafana.com/docs/grafana/latest/features/datasources/postgres/)
- [Create Azure Log Analytics Workspace](https://docs.microsoft.com/azure/azure-monitor/learn/quick-create-workspace) 
