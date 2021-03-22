<properties
  pagetitle="Server down after planned maintenance completed"
  description="Server down after planned maintenance completed"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788517"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="0d37e6c4-53fe-4ba6-a996-ab4219941726"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Azure Database for MySQL Server down after planned maintenance completed

## Quick tips

A planned maintenance for a given Azure region is typically expected to run 15 hrs. The window also includes buffer time to execute a rollback plan, if necessary. During planned maintenance, database server restarts or failovers can occur. These might lead to brief periods when the database servers are unavailable for end users.

Azure Database for MySQL servers run in containers, so typically database server restarts are quick and complete within 60-120 seconds. The entire planned maintenance event, including the restart of each server, is carefully monitored by the engineering team. The duration of server failover is dependent on database recovery time, so if there is heavy transactional activity on the server at the time of failover, it may take longer for the database to come online. To avoid longer restart times, it is recommended to avoid any long running transactions (bulk loads) during planned maintenance events.

In summary, while the planned maintenance event runs for 15 hours, the individual server impact generally lasts 60 seconds, depending on the transactional activity on the server. A notification is sent to customers 72 calendar hours before planned maintenance starts, followed by a second notification when maintenance is in progress for a given region.

## **Recommended documents**

* [Planned maintenance - duration and customer impact](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#planned-maintenance---duration-and-customer-impact)
* [How can I get notified of planned maintenance?](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#how-can-i-get-notified-of-planned-maintenance)
