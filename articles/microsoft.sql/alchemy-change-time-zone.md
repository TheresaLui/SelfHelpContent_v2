 
<properties
pageTitle="How Do I Change SQL DB Timezone"
description="How Do I Change SQL DB Timezone"
ms.author="keithelm"
displayOrder=""
articleId="89BBAD15-E75C-4661-B316-7A0BA77D1636"
selfHelpType="Apollo"
supportTopicIds="3d780dd5-7558-b609-a634-c8221b70709d"
productPesIds="13491"
cloudEnvironments="public"
ownershipId="AzureData_AzureSQLDB"
/>

# How Do I Change SQL DB Timezone 
 

## SQL DB Time Zone Configuration 

All Azure SQL Database logical servers, regardless of region, are configured to use Coordinated Universal Time (UTC) as the local time zone. This setting cannot be configured by the user. If your applicable requires datetime values in a specific local time zone, your options are to:
- Use the [AT TIME ZONE](https://docs.microsoft.com/sql/t-sql/queries/at-time-zone-transact-sql?view=sql-server-ver15) T-SQL clause to convert UTC to the desired time zone. In some simple queries, you might be able to include this conversion inside a scalar function, but this might cause performance problems on more complex queries. A better performing option is to do this directly in the query, as shown in [this blog](https://blog.greglow.com/2020/03/12/sql-getting-local-date-and-time-in-azure-sql-database/).
- Change your data tier to store UTC (or datetimeoffset) timestamps, and change the application tier to convert timestamps to user local time
- If you have the flexibility to choose between SQL Database or SQL Managed Instance, note that SQL Managed Instance supports [specifying the local time zone](https://docs.microsoft.com/azure/azure-sql/managed-instance/timezones-overview) at instance creation. 