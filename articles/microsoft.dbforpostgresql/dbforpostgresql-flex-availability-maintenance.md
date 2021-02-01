<properties
    pageTitle="Maintenance for Azure Database for PostgreSQL - flexible server"
    description="Managing networing for Azure Database for PostgreSQL - flexible server"
    service="microsoft.dbforpostgresql"
    resource="flexibleServers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="50"
    selfHelpType="generic"
    supportTopicIds="32780966"
    resourceTags="servers, databases"
    productPesIds="17069"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-flex-availability-maintenance"
	ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Scheduled maintenance in Azure Database for PostgreSQL – Flexible server

## **Recommended Steps**

* You can define different maintenance schedules for each flexible server in your Azure subscription
* When specifying preferences for the maintenance schedule, you can pick a day of the week and a start time window. If you don't specify times, the system will pick times between 11pm and 7am in your server's region time.
* Notifications are delivered via Azure Health Service
* You can receive notifications about upcoming scheduled maintenance via the following:
   * Email to a specific address
   * Email to an Azure Resource Manager Role 
   * Text message (SMS) to mobile devices
   * Pushed as a notification to an Azure app
   * Delivered as a voice message
* Usually there are at least 30 days between successful scheduled maintenance events for a server. However, in case of a critical emergency update, such as a severe vulnerability, the notification window could be shorter than five days. The critical update may be applied to your server even if a successful scheduled maintenance was performed in the last 30 days.
