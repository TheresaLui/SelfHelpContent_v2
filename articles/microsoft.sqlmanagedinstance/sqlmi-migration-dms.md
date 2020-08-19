<properties
	pageTitle="Migrating to Azure|Database migration service (DMS)"
	description="Migrating to Azure|Database migration service (DMS)"
	service="microsoft.sql"
	resource="servers"
	authors="MladjoA"
    ms.author="mlandzic"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32637255"
	productPesIds="16259"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="48edeb33-20e6-410c-945d-a23e04d24a16"
	ownershipId="AzureData_AzureSQLMI"
/>

# Database migration service

You can use the Azure Database Migration Service to migrate the databases from an on-premises SQL Server instance to an Azure SQL Database Managed Instance. When you migrate databases to Azure by using Azure Database Migration Service, you can do an offline or an online migration. With an offline migration, application downtime starts when the migration starts. With an online migration, downtime is limited to the time to cut over at the end of migration. We suggest that you test an offline migration to determine whether the downtime is acceptable; if not, do an online migration.

## **Recommended Steps**
- Ensure that your VNet Network Security Group rules don't block the following inbound communication ports to Azure Database Migration Service: 443, 53, 9354, 445, 12000. For more detail on Azure VNet NSG traffic filtering, see [Filter network traffic with network security groups](https://docs.microsoft.com/azure/virtual-network/virtual-networks-nsg).
- Configure your [Windows Firewall for source database engine access](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-a-windows-firewall-for-database-engine-access).
- Open your Windows Firewall to allow the Azure Database Migration Service to access the source SQL Server, which by default is TCP port 1433.
- If you're running multiple named SQL Server instances using dynamic ports, you may wish to enable the SQL Browser Service and allow access to UDP port 1434 through your firewalls so that the Azure Database Migration Service can connect to a named instance on your source server.
- If you're using a firewall appliance in front of your source databases, you may need to add firewall rules to allow the Azure Database Migration Service to access the source database(s) for migration, as well as files via SMB port 445.
- Ensure that the logins used to connect the source SQL Server and the target managed instance are members of the sysadmin server role.
- Provide an SMB network share that contains full database backup files and subsequent transaction log backup files the Azure Database Migration Service can use for database migration.
- Ensure that the service account running the source SQL Server instance has write privileges on the network share that you created and that the computer account for the source server has read/write access to the same share.

## **Recommended Documents**

- [Tutorial: Migrate SQL Server to an Azure SQL Database managed instance online using DMS](https://docs.microsoft.com/azure/dms/tutorial-sql-server-managed-instance-online)
- [Tutorial: Migrate SQL Server to an Azure SQL Database managed instance offline using DMS](https://docs.microsoft.com/azure/dms/tutorial-sql-server-to-managed-instance)
- [Network topologies for Azure SQL DB Managed Instance migrations using the Azure Database Migration Service](https://docs.microsoft.com/azure/dms/resource-network-topologies)<br>
