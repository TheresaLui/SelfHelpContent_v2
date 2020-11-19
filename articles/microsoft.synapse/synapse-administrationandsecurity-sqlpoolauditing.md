<properties
  pagetitle="Administration and Security/SQL pool Auditing"
  service="microsoft.synapse"
  resource="sqlpools"
  ms.author="saltug,goventur"
  selfhelptype="Generic"
  supporttopicids="32738814"
  resourcetags=""
  productpesids="15818"
  cloudenvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
  articleid="synapse-administrationandsecurity-sqlpoolauditing"
  ownershipid="AzureData_SQLDataWarehouse" />
# Administration and Security/SQL pool Auditing

## **Recommended Steps**

* **Can [fn_get_audit_file()](https://docs.microsoft.com/sql/relational-databases/system-functions/sys-fn-get-audit-file-transact-sql?view=azure-sqldw-latest) be used to read audit files from Synapse databases?**
  Yes, but the connection needs to be established to the logical server master database, or to an SQL DB database, and not to a Synapse database.

* **Cannot enable Auditing feature for Synapse Workspace resource, only for Synapse SQL DW.**
  Auditing and Advanced threat detection is not available for Synapse Workspace SQL Pools yet. Please note that Synapse Workspace is in Preview and not all options are available yet.

## **Recommended Documents**

For getting started with auditing, refer to [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/) document.

For other security capabilities, refer to these documents:

* [SQL Pool Security Overview](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-overview-manage-security/)
* [Auditing - servers, pools, and databases](https://docs.microsoft.com/azure/sql-database/sql-database-auditing?WT.mc_id=pid:13491:sid:32630407/)
* [Advanced data security](https://docs.microsoft.com/azure/sql-database/sql-database-advanced-data-security)