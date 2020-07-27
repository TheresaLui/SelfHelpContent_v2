<properties
	selfHelpType = "generic"
	cloudEnvironments = "public, fairfax, blackforest, mooncake, usnat, ussec"
	ownershipId = "AzureData_SQLDataWarehouse"
	service = "microsoft.synapse"
	resource = "sqlPools"
	resourceTags = ""
	productPesIds = "15818"
	supportTopicIds = "32738770"
	displayOrder = ""
	diagnosticScenario = ""
	infoBubbleText = ""
	pageTitle = "Connectivity/Error connecting to SQL pool database"
	description = "Connectivity/Error connecting to SQL pool database"
	articleId = "synapse-connectivity-errorconnectingtosqlpooldatabase-new-st"
	authors = "saltug"
	ms.author = "saltug"
/>

# Connectivity/Error connecting to SQL pool database

Issues connecting to SQL Data Warehouse can occur for a number of reasons, including incorrect firewall configuration, connection strings, or maintenance periods. Follow the [connectivity troubleshooting guide](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity).

If you are having issues with a client tool, please ensure you have the latest version of the tool and [review the documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot#tools).

## **Recommended Steps**

### **Use the connectivity troubleshooter**

In the Azure Portal, go to the SQL Data Warehouse you are trying to connect and click on the **Diagnose and solve problems** on the left navigation pane.  Click on the **Troubleshoot** button under **How to troubleshoot availability and connectivity issues**.

### **Check for Azure service outages**

Click on the [Microsoft Azure Service Dashboard](https://azure.microsoft.com/status/) to see if there are any known issues.

### **Check for service availability**

Check to see if your service is available. In the Azure portal, go to the SQL Data Warehouse you are trying to connect and click **Diagnose and solve problems** on the left navigation.  See [troubleshooting documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#check-service-availability) for more details.

### **Check for paused or scaling operation**

Check to see if your service is currently paused or in the process of scaling. Open the **Azure Portal** and go to your SQL Data Warehouse you are trying to connect. See [troubleshooting documentation](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#check-for-paused-or-scaling-operation) for more details.

### **Check resource health blade in the Azure Portal for status updates**

A status of Unavailable means that Resource Health has detected consistent login failures due to system error on your SQL Database. A status of Degraded means that Resource Health has detected a majority of successful logins, but some failures as well. These login failures may be caused by transient errors.

### **Check your firewall settings**

SQL Data Warehouse communicates over port 1433. If you're trying to connect from within a corporate network, outbound traffic over port 1433 might not be allowed by your network's firewall. In that case, you can't connect to your Azure SQL Database server unless your IT department opens port 1433. [Click here for additional information](https://docs.microsoft.com/azure/sql-database/sql-database-firewall-configure#create-and-manage-ip-firewall-rules).

### **Check your VNet/Service Endpoint settings**

If you're receiving [errors **40914** and **40615**](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#check-your-vnetservice-endpoint-settings), see error description and resolution below in the common error messages section. 

### **Check for the latest drivers**

Check to see that you are using the [latest version of the tool and drivers](https://docs.microsoft.com/sql/connect/jdbc/system-requirements-for-the-jdbc-driver?view=sql-server-2017) to connect to your SQL Data Warehouse. [Click here for additional information](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#check-for-the-latest-drivers).

### **Check your connection string**

Check to make sure your connection strings are set properly. [Click here](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#check-your-connection-string) to view some sample connection strings for ADO.NET, ODBC, PHP, and JDBC. You can find additional information around [connection strings here](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-connect-overview#find-your-server-name).

### **Intermittent connection issues**

Check to see if you're experiencing heavy load on the server with a high number of queued requests. You may need to scale up your data warehouse for additional resources. [Click here for additional information.](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity#intermittent-connection-issues) Try implementing a [retry logic](https://docs.microsoft.com/azure/sql-database/sql-database-connectivity-issues#retry-logic-for-transient-errors) in your client application to help mitigate these situations and should generally make the errors transparent to the end user.

### **Common Error Messages**

* **Error: Login failed for user 'NT AUTHORITY\ANONYMOUS LOGON'. (Microsoft SQL Server, Error: 18456)**

    This error occurs when an AAD user tries to connect to the master database, but does not have a user in master. To correct this issue, either specify the SQL Data Warehouse you wish to connect to at connection time or add the user to the master database. See Security overview article for more details.

* **Error: The server principal "MyUserName" is not able to access the database "master" under the current security context. Cannot open user default database. Login failed. Login failed for user 'MyUserName'. (Microsoft SQL Server, Error: 916)**

    This error occurs when an AAD user tries to connect to the master database, but does not have a user in master. To correct this issue, either specify the SQL Data Warehouse you wish to connect to at connection time or add the user to the master database. See Security overview article for more details.

* **Error 40914: Cannot open server '[server-name]' requested by the login. Client is not allowed to access the server**

    The client is in a subnet that has virtual network server endpoints. But the Azure SQL Database server has no virtual network rule that grants to the subnet the right to communicate with the SQL Database. On the Firewall pane of the Azure portal, use the virtual network rules control to [add a virtual network rule](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json#anchor-how-to-by-using-firewall-portal-59j) for the subnet.

* **Error 40615: Cannot open server '{0}' requested by the login. Client with IP address '{1}' is not allowed to access the server**

    The client is trying to connect from an IP address that is not authorized to connect to the Azure SQL Database server. The server firewall has no IP address rule that allows a client to communicate from the given IP address to the SQL Database. Enter the client's IP address as an IP rule. Do this by using the Firewall pane in the Azure portal. A list of several SQL Database error messages is documented [here](https://docs.microsoft.com/azure/sql-database/sql-database-develop-error-messages).

* **Error: 'The transaction log for database 'xxxx' is full due to 'ACTIVE_TRANSACTION'. (Microsoft SQL Server, Error: 9002)'**

    This error usually means there is a long running transaction that is not committed yet or there is a hanging session, which makes transaction log full. Check for hanging sessions with SELECT * FROM sys.dm_exec_sessions and kill it with KILL <session_id>. If there is no hanging sessions, you may need to cancel the long running query or kill that session to mitigate this issue.

## **Recommended Documents**

* [Troubleshooting connectivity issues](https://docs.microsoft.com/azure/sql-data-warehouse/sql-data-warehouse-troubleshoot-connectivity)
* [Available PowerShell commands](https://docs.microsoft.com/powershell/module/azurerm.sql/?view=azurermps-6.3.0#sql)
* [Configure Azure AD authentication](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)
* [Configure multi-factor authentication for Azure AD](https://docs.microsoft.com/azure/sql-database/sql-database-ssms-mfa-authentication-configure?WT.mc_id=pid:13491:sid:32745423/)
* [Additional Troubleshooting](https://azure.microsoft.com/documentation/articles/sql-data-warehouse-troubleshoot/)
* [Create a server-level firewall rule](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal#create-a-server-level-firewall-rule)
* [Use virtual network service endpoints](https://docs.microsoft.com/azure/sql-database/sql-database-vnet-service-endpoint-rule-overview?toc=/azure/sql-data-warehouse/toc.json)
* [View maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/viewing-maintenance-schedule)
* [Change maintenance schedule](https://docs.microsoft.com/azure/sql-data-warehouse/changing-maintenance-schedule)
* [Connect and manage your Data Warehouse using the Azure portal](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-portal)
* [Connect and manage your Data Warehouse using PowerShell](https://docs.microsoft.com/azure/sql-data-warehouse/create-data-warehouse-powershell)


