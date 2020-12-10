<properties
  pagetitle="Database Mirroring: Common issues for AlwaysOn, High Availability, and disaster recovery "
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740078"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="797e35a7-15dc-4a6b-a285-a2a7e4f80eff"
  ownershipid="AzureData_AzureSQLVM" />
# Database Mirroring: Common issues for AlwaysOn, High Availability, and disaster recovery 

## Resolve Database Mirroring issues for AlwaysOn, High Availability, and disaster recovery

Use this article to resolve many common Database Mirroring issues. 

* **"Error: The server network address 'TCP://server1.test.local:5022' cannot be reached or does not exist"**

    For **Mirroring Synchronization**, make sure to set the correct [**Server Network** address and **Port**](https://docs.microsoft.com/sql/database-engine/database-mirroring/specify-a-server-network-address-database-mirroring?view=sql-server-ver15#Examples). Ensure that the Windows Firewall and Network Security Groups on Azure are not blocking the **Mirroring Ports**.

* **"Error: 1479: The mirroring connection to 'TCP://server1.test.local:5022' has timed out for database 'DBname' after 10 seconds without a response."**
   
    Connection timeouts can result from [SQL performance]( https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices), [storage throttling]( https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics), and network issues. While you investigate the main issue, you can temporarily work around the issue by increasing the [**Partner Timeout**](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-database-mirroring?view=sql-server-ver15#syntax) setting (default is 10 seconds), as follows:
     
    ```SQL
     ALTER DATABASE (database) SET PARTNER TIMEOUT (Number of Seconds)
    ```
    
* **"Error Database Mirroring login attempt by user 'Domain\User$.' failed with the error: 'Connection handshake failed. The login 'Domain\User$' does not have CONNECT permission on the endpoint."**
    
    Setting up Mirroring requires the **Alter** permission on the database and the **Create endpoint** permission, or membership in the sys admin fixed server role. Make sure that the **ports** are open for communication for Mirroring endpoints and the SQL Instance. Make sure that the SQL Service account is added to SQL. Grant connect permission to the mirroring endpoint to the user, as follows:
      
    ```SQL
      GRANT CONNECT ON ENDPOINT::Endpoint_Mirroring TO [Domain\Login];
    ```

* **Mirror Server Database is Disconnected/In Recovery**

    Make sure that the [endpoints are configured correctly]( https://docs.microsoft.com/sql/database-engine/database-mirroring/troubleshoot-database-mirroring-configuration-sql-server?view=sql-server-ver15#Endpoints). If you have set up database mirroring with Certificates, make sure that the certificates are not expired and that [Outbound connections are set up correctly](https://docs.microsoft.com/sql/database-engine/database-mirroring/example-setting-up-database-mirroring-using-certificates-transact-sql?redirectedfrom=MSDN&view=sql-server-ver15#ConfiguringOutboundConnections).

* **Mirror Server Database is in Suspended state**

    To determine why the database moved to a Suspended state, check the error log. You also can try to [pause or resume the Mirroring](https://docs.microsoft.com/sql/database-engine/database-mirroring/pause-or-resume-a-database-mirroring-session-sql-server?view=sql-server-ver15). If nothing is recorded in the error log, it's likely that there is [storage throttling]( https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics) or other SQL performance issues on the server. If you have VM-level throttling, upsizing the VM can help.

* **Review Mirroring basics and pre-requisites**

   * For a mirroring session to be established, the partners and the witness (if any) must be running on the [same or a higher version of SQL Server](https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Prerequisites). The database must be in full recovery mode to set up Mirroring.

   * Review the [Prerequisites]( https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Prerequisites) and [Restrictions](https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Restrictions) for Database Mirroring.

## **Recommended Documents**

* [Setup Login accounts for Database Mirroring](https://docs.microsoft.com/sql/database-engine/database-mirroring/set-up-login-accounts-database-mirroring-always-on-availability?view=sql-server-ver15)
* [Configure Database Mirroring using Windows Authentication](https://docs.microsoft.com/sql/database-engine/database-mirroring/database-mirroring-establish-session-windows-authentication?view=sql-server-ver15)
* [Configure Database Mirroring using Certificates](https://docs.microsoft.com/sql/database-engine/database-mirroring/example-setting-up-database-mirroring-using-certificates-transact-sql?view=sql-server-ver15)
* [Database Mirroring Operating Modes](https://docs.microsoft.com/sql/database-engine/database-mirroring/database-mirroring-operating-modes?view=sql-server-ver15)
* [Troubleshoot Database Mirroring Configuration](https://docs.microsoft.com/sql/database-engine/database-mirroring/troubleshoot-database-mirroring-configuration-sql-server?view=sql-server-ver15)
* [Database Mirroring Failover Fails with Error 3456](https://support.microsoft.com/help/4042251/fix-database-mirroring-failover-fails-with-error-3456-in-sql-server)
* [High availability and disaster recovery for SQL Server in Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-high-availability-dr)
