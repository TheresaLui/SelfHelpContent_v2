<properties
  pagetitle="Linked Server, Distributed queries"
  description="Linked Server, Distributed queries"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740082"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="ff1d2b08-2e5a-4b83-a708-438b3d5aa225"
  ownershipid="AzureData_AzureSQLVM" />
# Linked Server, Distributed queries

4 out of 5 customers are able to resolve their issues with Linked Server, Distributed queries using the following steps.

## **Recommended Steps**

**To avoid Linked server issues, ensure that**
- SQL Server and its components are [up to date to the latest build](https://support.microsoft.com/help/321185/how-to-determine-the-version-edition-and-update-level-of-sql-server-an)
- Linked server is [created correctly](https://docs.microsoft.com/sql/relational-databases/linked-servers/create-linked-servers-sql-server-database-engine?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)
- Ensure that SQL port (by default 1433) is [open in NSG and in firewall](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/ways-to-connect-to-sql#connection-scenarios) 
- If possible, run the [third-party provider in out-of-process mode by not setting "Allow inprocess"](https://docs.microsoft.com/archive/blogs/dataaccesstechnologies/permissions-needed-to-set-up-linked-server-with-out-of-process-provider) in order to avoid unexpected behavior

## **Recommended Documents**

- Linked Servers [Overview](https://docs.microsoft.com/sql/relational-databases/linked-servers/linked-servers-database-engine?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support)
- [Create](https://docs.microsoft.com/sql/relational-databases/linked-servers/create-linked-servers-sql-server-database-engine?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support) Linked Servers
- Set up and troubleshoot a [linked server to an Oracle database](https://docs.microsoft.com/troubleshoot/sql/admin/set-up-troubleshoot-linked-server)
- How SQL Server [query processor interacts with an OLE DB provider](https://docs.microsoft.com/sql/relational-databases/linked-servers/create-linked-servers-sql-server-oledb-provider?view=sql-server-ver15) 
- [Ad hoc distributed queries](https://docs.microsoft.com/sql/database-engine/configure-windows/ad-hoc-distributed-queries-server-configuration-option?view=sql-server-ver15&WT.mc_id=Portal-Microsoft_Azure_Support) Server Configuration Option
- [Distributed Queries – Remote Login Permissions and Execution Plans](https://techcommunity.microsoft.com/t5/sql-server-support/distributed-queries-8211-remote-login-permissions-and-execution/ba-p/315828)