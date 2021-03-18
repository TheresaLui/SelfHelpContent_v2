<properties
  pagetitle="Configuring maintenance window"
  description=""
  service="microsoft.sql"
  resource="servers"
  ms.author="mlandzic,vitomaz"
  selfhelptype="Generic"
  supporttopicids="32785985"
  productpesids="13491"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="sql-maintenance-config-window"
  ownershipid="AzureData_AzureSQLDB" />
# Configuring maintenance window

The Maintenance window feature is available to eligible Azure offers in select regions. 
Configuring or changing the maintenance window will initiate database failover, which may cause a few seconds of unavailability.

## **Recommended Steps**

1. Check [the list of regions](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window#azure-region-support) where maintenance window is available
2. Check whether Azure subscription type is [eligible](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window#cost-and-eligibility) for the maintenance window feature
3. Maintenance window configuration requires database failover at the end of the process. Make sure to run it outside of the peak business hours
4. To get the maximum benefit from maintenance windows, make sure your client applications are using the [redirect connection policy](https://docs.microsoft.com/azure/azure-sql/database/connectivity-architecture#connection-policy). Any connections using the proxy connection policy could be affected by both the chosen maintenance window and a gateway node maintenance window.

## **Recommended Documents**

* [About maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window)
* [Configure maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window-configure)
* [Frequently asked questions for maintenance window](https://docs.microsoft.com/azure/azure-sql/database/maintenance-window-faq)
