<properties
  pagetitle="Scheduled maintenance in Azure Database for MySQL – Flexible server&#xD;"
  description="Scheduled maintenance in Azure Database for MySQL – Flexible server"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="ambhatna,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747623"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="2c33c8ed-b4a5-48da-9863-f5e5424b97ed"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Scheduled maintenance in Azure Database for MySQL – Flexible server

### Considerations

* You can define different maintenance schedules for each flexible server in your Azure subscription.
* When specifying preferences for the maintenance schedule, you can pick a day of the week and a time window. If you don't specify, the system will pick times between 11pm and 7am in your server's region time.
* You can have notifications about upcoming scheduled maintenance emailed to a specific address or to an Azure Resource Manager Role, sent in a text message (SMS) to mobile devices, pushed as a notification to an Azure app, and delivered as a voice message.
* Normally there are at least 30 days between successful scheduled maintenance events for a server. However, in case of a critical emergency update such as that to update a severe vulnerability, the notification window could be shorter than five days. A critical update can be applied to your server even if a successful scheduled maintenance was performed within the last 30 days.

## **Recommended documents**

* [Scheduled maintenance in Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-maintenance)
* [Manage scheduled maintenance settings for Azure Database for MySQL – Flexible server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal)