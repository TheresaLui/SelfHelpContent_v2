<properties
  pagetitle="Portal and client tools/azure portal"
  description="portal and client tools/azure portal"
  service="microsoft.sql"
  resource="servers"
  ms.author="emlisa,babarmav"
  selfhelptype="Generic"
  supporttopicids="32630412"
  resourcetags=""
  productpesids="13491"
  cloudenvironments="public,blackforest,fairfax,mooncake,usnat,ussec"
  articleid="a4981f93-f5da-4990-8877-a0ec3abc3489"
  ownershipid="AzureData_AzureSQLDB_Portal" />
# Portal and client tools/azure portal

## **Recommended Steps**
Most users can resolve issues concerning by using the following steps:

**How Do I move SQL Resource?**
* [Move resources to a new resource group or subscription](https://docs.microsoft.com/azure/azure-resource-manager/management/move-resource-group-and-subscription#next-steps) 
* [Move resources to new region - Azure SQL Database & Azure SQL Managed Instance](https://docs.microsoft.com/azure/azure-sql/database/move-resources-across-regions?toc=/azure/azure-resource-manager/management/toc.json)
* Currently, you cannot move SQL Managed Instance resources.  Refer to [Move operation support for resources for supported resources that can be moved](https://docs.microsoft.com/azure/azure-sql/database/move-resources-across-regions?toc=/azure/azure-resource-manager/management/toc.json)


***How Do I Change SQL DB Timezone***

All Azure SQL Database logical servers, regardless of region, are configured to use Coordinated Universal Time (UTC) as the local time zone. This setting cannot be configured by the user. If your applicable requires datetime values in a specific local time zone, your options are to:

- Use the [AT TIME ZONE](https://docs.microsoft.com/sql/t-sql/queries/at-time-zone-transact-sql?view=sql-server-ver15) T-SQL clause to convert UTC to the desired time zone. In some simple queries, you might be able to include this conversion inside a scalar function, but this might cause performance problems on more complex queries. A better performing option is to do this directly in the query, as shown in [this blog](https://blog.greglow.com/2020/03/12/sql-getting-local-date-and-time-in-azure-sql-database/).
- Change your data tier to store times as datetimeoffset values (offset will be zero since it is UTC), and change the application tier to convert datetimeoffset to user local time
- If you have the flexibility to choose between SQL Database or SQL Managed Instance, note that SQL Managed Instance supports [specifying the local time zone](https://docs.microsoft.com/azure/azure-sql/managed-instance/timezones-overview) at instance creation.


**Issues related to connecting to Query Editor (Preview)**

Issues related connecting to the Query Editor, check the following:
- Outbound HTTPS traffic for ports 443 and 1443 are enabled. The query editor uses ports 443 and 1443 to communicate.
- The client IP address (the IP address that you are connecting from) has been added to the [server firewall rule](https://docs.microsoft.com/azure/azure-sql/database/firewall-create-server-level-portal-quickstart).
- If you have configured [Private Link](https://docs.microsoft.com/azure/azure-sql/database/private-endpoint-overview) connection to Azure SQL Database, server firewall rule is not required.
- For additional documentation refer to [Quickstart: Use the Azure portal's query editor (preview) to query an Azure SQL Database](https://docs.microsoft.com/azure/azure-sql/database/connect-query-portal#query-editor-considerations)


***Troubleshooting issues in Azure Portal***
capture a browser trace for troubleshooting, refer to [ Capture a browser trace for troubleshooting on how to capture a browser trace](https://docs.microsoft.com/azure/azure-portal/capture-browser-trace).

## **Recommended Documents**

- [Query editor considerations](https://docs.microsoft.com/azure/sql-database/sql-database-connect-query-portal?WT.mc_id=pid:13491:sid:32630412/#query-editor-considerations)