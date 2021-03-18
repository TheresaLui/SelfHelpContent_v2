<properties
  pagetitle="Maintenance event outside of maintenance window"
  description=""
  service="microsoft.sql"
  resource="servers"
  ms.author="mlandzic,vitomaz"
  selfhelptype="Generic"
  supporttopicids="32785987"
  productpesids="13491"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="sql-maintenance-event-outside.window"
  ownershipid="AzureData_AzureSQLDB" />
# Maintenance event outside of maintenance window

Did you notice a connectivity glitch or unavailability signal outside of the maintenance window? <br>
This may happen because of:<br> 

* Hardware failure (unplanned failover)
* [Scaling operations](https://docs.microsoft.com/azure/azure-sql/database/scale-resources)
* [Gateway maintenance](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window#gateway-maintenance-for-azure-sql-database)
* [User-initiated failover](https://docs.microsoft.com/azure/azure-sql/database/high-availability-sla#testing-application-fault-resiliency)
* In very rare circumstances, this occurs because of an urgent security patch that couldn't be postponed until the next maintenance window.

## **Recommended Steps**

* Check the [Resource Health history](https://docs.microsoft.com/azure/azure-sql/database/resource-health-to-troubleshoot-connectivity) of your database for more details

## **Recommended Documents**

* [About maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window)
* [Frequently asked questions about maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window-faq)
* [Prepare for maintenance events](https://docs.microsoft.com/azure/azure-sql/database/planned-maintenance)
