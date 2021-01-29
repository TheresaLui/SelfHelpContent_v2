<properties
    pageTitle="Logs on Azure Database for PostgreSQL - Hyperscale (Citus)"
    description="Logs on Azure Database for PostgreSQL - Hyperscale (Citus)"
    service="microsoft.dbforpostgresql"
    resource=""
    ms.author="raagyema"
    displayOrder="70"
    articleId="dbforpostgresql-hyperscale-monitor-logs.md"
    selfHelpType="generic"
    supportTopicIds="32640020"
    resourceTags=""
    productPesIds="17068"
    cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# PostgreSQL logs

Azure Database for PostgreSQL - Hyperscale (Citus) logs are available via [Azure Monitor Logs, storage account, or Event Hubs](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings). The log format is JSON; each log event is represented by a JSON object. 

## **Recommended Steps**
* To configure logging
   1. Go to the portal page for your Hyperscale server
   2. Select *Diagnostic settings* and follow the prompts

* To configure logging using the Azure CLI, ARM Template, or other API, visit [the diagnostic settings](https://docs.microsoft.com/azure/azure-monitor/platform/diagnostic-settings) article 

* If you are using Azure Monitor Logs, you can query logs, create charts, and alert on log events. [Learn more about using Azure Monitor Logs](https://docs.microsoft.com/azure/azure-monitor/platform/data-platform-logs).

* Audit logging is not available in Hyperscale (Citus)
