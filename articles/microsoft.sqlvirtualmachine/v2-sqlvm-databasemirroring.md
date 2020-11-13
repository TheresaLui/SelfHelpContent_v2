<properties
  pagetitle="AlwaysOn, High Availability, Disaster Recovery - Database Mirroring"
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
# AlwaysOn, High Availability, Disaster Recovery - Database Mirroring

4 out of 5 customers are able to resolve their Database Mirroring issues using the following steps.

## **Recommended Steps**

* **Common Issues faced when Configuring or Troubleshooting Mirroring**

  * **Error: The server network address 'TCP://server1.test.local:5022' can not be reached or does not exist**

    It is important to set the correct [Server Network address and Port](https://docs.microsoft.com/sql/database-engine/database-mirroring/specify-a-server-network-address-database-mirroring?view=sql-server-ver15#Examples) for Mirroring Synchronization. Make sure Mirroring Ports are not blocked by Windows Firewall or Network Security Groups on Azure.

  * **Error: 1479 :The mirroring connection to "TCP://server1.test.local:5022" has timed out for database "DBname" after 10 seconds without a response.**
   
     Connection timeouts can be due to [SQL Performance]( https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/performance-guidelines-best-practices),  [Storage throttling]( https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics), or network issues. While you investigate the main issue, you can temporarily work around the issue by increasing the [Partner Timeout](https://docs.microsoft.com/sql/t-sql/statements/alter-database-transact-sql-database-mirroring?view=sql-server-ver15#syntax) setting from the default value of 10 seconds, as follows:
     
     ```SQL
     ALTER DATABASE <database> SET PARTNER TIMEOUT <Number of Seconds>
      ```
    
   * **Error Database Mirroring login attempt by user 'Domain\User$.' failed with error: 'Connection handshake failed. The login 'Domain\User$' does not have CONNECT permission on the endpoint.**
    
      Setting up Mirroring requires **ALTER** permission on the database and **CREATE ENDPOINT** permission, or membership in the sys admin fixed server role. Make sure **Ports** are open for communication for Mirroring endpoints and SQL Instance. Make sure the SQL Service account is added to SQL. Grant connect permission to the mirroring endpoint to the user, as follows:
      
      ```SQL
      GRANT CONNECT ON ENDPOINT::Endpoint_Mirroring TO [Domain\Login];
      ```

* **Mirror Server Database is Disconnected/In Recovery**

     Make sure the [Endpoints are configured correctly]( https://docs.microsoft.com/sql/database-engine/database-mirroring/troubleshoot-database-mirroring-configuration-sql-server?view=sql-server-ver15#Endpoints). If you have setup database mirroring with Certificates, please make sure that certificates are not expired and [Outbound connections are setup correctly](https://docs.microsoft.com/sql/database-engine/database-mirroring/example-setting-up-database-mirroring-using-certificates-transact-sql?redirectedfrom=MSDN&view=sql-server-ver15#ConfiguringOutboundConnections).

  * **Mirror Server Database is in Suspended state**

    You need check the error log why the database moved to Suspended state. You also can try to [Pause or Resume the Mirroring](https://docs.microsoft.com/sql/database-engine/database-mirroring/pause-or-resume-a-database-mirroring-session-sql-server?view=sql-server-ver15). If there is nothing recorded in the error log, it's likely that there is [Storage Throttling]( https://docs.microsoft.com/azure/virtual-machines/windows/disk-performance-windows#storage-io-utilization-metrics) or other SQL performance issues on the server. If you have VM-level throttling, upsizing the VM can help.

* **Mirroring Facts and Pre-requisites**

  * For a mirroring session to be established, the partners and the witness, if any, must be running on the [same or higher version of SQL Server](https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Prerequisites). The database must be in full recovery mode to set up Mirroring.

  * Review the [Prerequisites]( https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Prerequisites) and [Restrictions](https://docs.microsoft.com/sql/database-engine/database-mirroring/prerequisites-restrictions-and-recommendations-for-database-mirroring?view=sql-server-ver15#Restrictions) for Database Mirroring.


## **Recommended Documents**
* [Setup Login accounts for Database Mirroring](https://docs.microsoft.com/sql/database-engine/database-mirroring/set-up-login-accounts-database-mirroring-always-on-availability?view=sql-server-ver15)
* [Configure Database Mirroring using Windows Authentication](https://docs.microsoft.com/sql/database-engine/database-mirroring/database-mirroring-establish-session-windows-authentication?view=sql-server-ver15)
* [Configure Database Mirroring using Certificates](https://docs.microsoft.com/sql/database-engine/database-mirroring/example-setting-up-database-mirroring-using-certificates-transact-sql?view=sql-server-ver15)
* [Database Mirroring Operating Modes](https://docs.microsoft.com/sql/database-engine/database-mirroring/database-mirroring-operating-modes?view=sql-server-ver15)
* [Troubleshoot Database Mirroring Configuration](https://docs.microsoft.com/sql/database-engine/database-mirroring/troubleshoot-database-mirroring-configuration-sql-server?view=sql-server-ver15)
* [Database Mirroring Failover Fails with Error 3456](https://support.microsoft.com/help/4042251/fix-database-mirroring-failover-fails-with-error-3456-in-sql-server)
* [High availability and disaster recovery for SQL Server in Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-high-availability-dr)
