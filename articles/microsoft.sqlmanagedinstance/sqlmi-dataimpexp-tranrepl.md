<properties
	pageTitle="Features/Linked server"
	description="Features/Linked server."
	service="microsoft.sql"
	resource="servers"
	authors="jovanpop-msft"
    ms.author="jovanpop"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637312"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="03b89da5-61f4-4bd5-8704-312b1fd649f2"
	ownershipId="AzureData_AzureSQLMI"
/>

# Transactional replication

Azure SQL Database Managed Instance enables you to replicate one or several tables into another Managed Instance, singleton SQL database, or SQL Server using [transactional replication](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transactional-replication). You can also replicate the changes from external Managed Instance, singleton SQL database, or SQL Server to local tables. This feature is currently in **preview mode** and there are some [known limitations](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#replication).

* More information about [configuration of transactional replication in Managed Instance](https://docs.microsoft.com/azure/sql-database/replication-with-sql-database-managed-instance)

## **Recommended Steps**

If you are experiencing some issues with transactional replication, the following steps can help you to find a way to troubleshoot the issues.

- Review the requirements for the [transactional replication in Managed Instance](https://docs.microsoft.com/azure/sql-database/replication-with-sql-database-managed-instance#requirements):

  - Managed instance is not participating in a geo-replication (failover group) relationship
  - Publisher managed instance is on the same virtual network as the distributor and the subscriber, or vNet peering has been established between the virtual networks of all three entities
  - Connectivity uses SQL Authentication between replication participants
  - You need an Azure Storage Account share for the replication working directory. Make sure that you have used [correct keys](https://docs.microsoft.com/azure/storage/common/storage-account-manage#access-keys) and use **backslash only** in the file share path. This is an example of incorrect path: \\replstorage.file.core.windows.net**/**replshare as slash is used.
  - Port 445 (TCP outbound) should be open in the security rules of NSG for the managed instances to access the Azure file share

- Check the [transactional replication constraints](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transact-sql-information#replication) in Managed Instances to identify are you using some unsupported feature (for example, [updateable subscriptions](https://docs.microsoft.com/sql/relational-databases/replication/transactional/updatable-subscriptions-for-transactional-replication))
- If you are experiencing connection/login timeout issues, you would need to [increase the timeout in the connection](https://docs.microsoft.com/azure/sql-database/replication-with-sql-database-managed-instance#9---modify-agent-parameters)
- Auto-failover groups should not be used if the Transactional Replication is configured

## **Recommended Documents**

- [Transactional replication](https://docs.microsoft.com/azure/sql-database/sql-database-managed-instance-transactional-replication)
- [Configure transactional replication in Managed Instance](https://docs.microsoft.com/azure/sql-database/replication-with-sql-database-managed-instance)
