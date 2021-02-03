<properties
    pageTitle="Scheduled maintenance in Azure Database for MySQL"
    description="Scheduled maintenance in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="500"
    selfHelpType="generic"
    supportTopicIds="32747990"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="35da5aa8-2c4a-44b7-95f9-49f0ccda7ab4"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Scheduled maintenance in Azure Database for MySQL

Azure Database for MySQL offers two deployment types - single server and flexible server. Scheduled maintenance feature is available only on the flexible server deployment type.

## **Recommended Steps**

* You can define different maintenance schedules for each flexible server in your Azure subscription.
* When specifying preferences for the maintenance schedule, you can pick a day of the week and a time window. If you don't specify, the system will pick times between 11pm and 7am in your server's region time.
* You can receive notifications about upcoming scheduled maintenance via emailed to a specific address, emailed to an Azure Resource Manager Role, sent in a text message (SMS) to mobile devices, pushed as a notification to an Azure app and delivered as a voice message.
* Normally there are at least 30 days between successful scheduled maintenance events for a server. However, in case of a critical emergency update such as a severe vulnerability, the notification window could be shorter than five days. The critical update may be applied to your server even if a successful scheduled maintenance was performed in the last 30 days.

## **Recommended Documents**

* Learn more about [scheduled maintenance in Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concept-maintenance)
* Learn how to [manage scheduled maintenance settings for Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal)