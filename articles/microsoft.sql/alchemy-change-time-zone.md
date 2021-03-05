 
<properties
pageTitle="How Do I Change SQL DB Timezone"
description="How Do I Change SQL DB Timezone"
ms.author="keithelm"
displayOrder=""
articleId="89BBAD15-E75C-4661-B316-7A0BA77D1636"
selfHelpType="Apollo"
supportTopicIds=""
productPesIds="13491"
cloudEnvironments="public"
ownershipId="AzureData_AzureSQLDB"
/>

# How Do I Change SQL DB Timezone 
 

## SQL DB Time Zone Configuration 

All Azure SQL Database logical servers, regardless of region, are configured with Coordinated Universal Time (UTC) as the local time zone.  This setting is not user configurable.  If your applicable expects datetime values to be in a specific local time zone, your options are:
- Use the [AT TIME ZONE](https://docs.microsoft.com/sql/t-sql/queries/at-time-zone-transact-sql?view=sql-server-ver15) clause to convert UTC to the desired time zone.  In some simple cases you may be able to encapsulate this conversion inside a scalar function, but this may cause performance problems on more complex queries.  A better performing option is to do this directly in the query, as shown in [this blog](https://blog.greglow.com/2020/03/12/sql-getting-local-date-and-time-in-azure-sql-database/).
- Make the change so that your data tier always persists UTC (or datetimeoffset) timestamps, and change the application tier to convert timestamps to user local time
- If you have flexibility between choosing SQL Database or SQL Managed Instance, note that SQL Managed Instance supports [specifying the local time zone](https://docs.microsoft.com/azure/azure-sql/managed-instance/timezones-overview) at instance creation. 