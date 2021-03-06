<properties
  pagetitle="Secure SQL applications in proxy mode"
  service="microsoft.network"
  resource="azurefirewalls"
  ms.author="Mario.Liu,mariliu"
  selfhelptype="Generic"
  supporttopicids="32745470"
  resourcetags=""
  productpesids="16556"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="d2a1bcc0-bc4e-49d3-b71c-121a9a5d9ee7"
  ownershipid="CloudNet_AzureFirewall" />
# Secure SQL applications in proxy mode

With SQL FQDNs, you can filter traffic:

- From your VNET to an Azure SQL Database or an Azure SQL Data Warehouse. For example, you may want to only allow access to `sql-server1.database.windows.net`.
- From on-premises to Azure SQL Managed Instances or SQL IaaS running in your VNETs
- From spoke-to-spoke to Azure SQL Managed Instances or SQL IaaS running in your VNETs

Note that SQL FQDN filtering is supported in proxy-mode only (port 1433). If you use SQL in the default redirect mode, you can filter access using the SQL service tag as part of network rules. If you use non-default ports for SQL IaaS traffic, you can configure those ports in the firewall application rules.

## **Recommended Documents**

- Learn more about [SQL FQDN filtering](https://docs.microsoft.com/azure/firewall/sql-fqdn-filtering)