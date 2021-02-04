<properties
  pagetitle="Scheduled maintenance in Azure Database for MySQL&#xD;"
  description="Scheduled maintenance in Azure Database for MySQL"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747990"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="35da5aa8-2c4a-44b7-95f9-49f0ccda7ab4"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Scheduled maintenance in Azure Database for MySQL

Azure Database for MySQL offers two deployment types: single server and flexible server. The scheduled maintenance feature is available only for the flexible server deployment type.

Most users can address the issues they encounter by considering the following points.

### Considerations

* You can define different maintenance schedules for each flexible server in your Azure subscription.
* When specifying preferences for the maintenance schedule, you can pick a day of the week and a time window. If you don't specify, the system will pick times between 11pm and 7am in your server's region time.
* You can have notifications about upcoming scheduled maintenance emailed to a specific address or to an Azure Resource Manager Role, sent in a text message (SMS) to mobile devices, pushed as a notification to an Azure app, or delivered as a voice message.
* Normally there are at least 30 days between successful scheduled maintenance events for a server. However, in case of a critical emergency update, such as that to update a severe vulnerability, the notification window could be shorter than five days. A critical update can be applied to your server even if a successful scheduled maintenance was performed within the last 30 days.

## **Recommended documents**

* [Scheduled maintenance in Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-maintenance)
* [Manage scheduled maintenance settings for Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal)