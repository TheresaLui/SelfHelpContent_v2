<properties
    pageTitle="Monitoring Azure Database for MySQL servers"
    description="Monitoring Azure Database for MySQL servers"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="230"
    selfHelpType="generic"
    supportTopicIds="32640071"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="b37c94dc-b937-4a82-bef5-7a39be09b7b9"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Monitoring Azure Database for MySQL servers

You can monitor your Azure Database for MySQL server using a default set of metrics through the Azure portal. You have the option to create alerts on these metrics, and have access to the MySQL slow query logs. Our integration with Azure Monitor Diagnostic Logs allows you to store the logs for a longer retention period and use third party tools to consume them.

## **Recommended Steps**

* Review the [supported list of metrics](https://docs.microsoft.com/azure/mysql/concepts-monitoring)
* Review how to [configure server logs](https://docs.microsoft.com/azure/mysql/concepts-server-logs)
* Set up the alert metrics [create alerts on metrics](https://docs.microsoft.com/azure/mysql/howto-alert-on-metric)

## **Recommended Documents**

* [Manage metric alerts using Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/platform/alerts-metric)<br>
* [Access server logs from the Azure portal](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-portal)<br>
* [Access server logs from the Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-server-logs-in-cli)
