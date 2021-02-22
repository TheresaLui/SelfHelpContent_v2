<properties
  pagetitle="Issue or errors in package execution"
  description=""
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="hecepeda"
  selfhelptype="Generic"
  supporttopicids="32749439"
  productpesids="14745"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="sqlvm-ssis-issue-errors-package-execution"
  ownershipid="AzureData_AzureSQLVM" />
# Issue or errors in package execution

The execution of an SSIS package may fail due to multiple reasons. We will discuss a few of the reasons in brief.


### Missing Windows privileges and rights

The Service Accounts running SSIS Service, SQL Server Agent Service, and SQL Server Agent Service require privileges at the Operating System level to execute SSIS packages. A lack of these permissions can impact: deployment of an SSIS package to SSISDB Catalog, execution of an SSIS package located in SSISDB Catalog, and execution of an SSIS package via SQL Server Agent job.

In addition, lack of permissions can generate errors, such as:

- "Error: System.ComponentModel.Win32Exception: A required privilege is not held by the client while Deploying SSIS Project."
- "Error: The process could not be created for step 1 of job (reason: A required privilege is not held by the client). The step failed."
- "Packages in SSISDB Catalog could be stuck in ‘Pending Execution’ state."

**To confirm** that the issue is happening because of missing privileges and rights, deploy a package to file system and run it using `DTExec`.


### Permissions required
Review the following lists for permission requirements in SSIS, SQL Server and SQL Server Agent service accounts.

- _SQL Server Database Engine_:<br>
   Log on as a service (**SeServiceLogonRight**)<br>
   Replace a process-level token (**SeAssignPrimaryTokenPrivilege**)<br>
   Bypass traverse checking (**SeChangeNotifyPrivilege**)<br>
   Adjust memory quotas for a process (**SeIncreaseQuotaPrivilege**)<br>

- _SQL Server Agent_:<br>
   Log on as a service (**SeServiceLogonRight**)<br>
   Replace a process-level token (**SeAssignPrimaryTokenPrivilege**)<br>
   Bypass traverse checking (**SeChangeNotifyPrivilege**)<br>
   Adjust memory quotas for a process (**SeIncreaseQuotaPrivilege**)<br>

- _SSIS_:<br>
   Log on as a service (**SeServiceLogonRight**)<br>
   Permission to write to application event log<br>
   Bypass traverse checking (**SeChangeNotifyPrivilege**)<br>
   Impersonate a client after authentication (**SeImpersonatePrivilege**)<br>

 To adjust these properties, under **Run** > `Secpol.msc` > **User Rights Assignment**

See Recommended documents for more information.

### **Memory-related issues**

The execution of an SSIS Package may fail with different errors suggesting the issue is memory related.

A few memory-related errors for SSIS Packages are as follows:

- "Not enough storage is available to complete this operation."
- "A buffer failed while allocating 10485760 bytes."
- "The system reports 2 percent memory load. There are 1,099,441,074,176 bytes of physical memory with 1074776596480 bytes free. There are 4294836224 bytes of virtual memory with 65310720 bytes free. The paging file has 1153128165376 bytes with 1124943544320 bytes free."
- "The attempt to add a row to the Data Flow task buffer failed with error code **0x8007000E.**"

If an SSIS Package fails due to memory related issues, ensure that best practices for SSIS Package development have been followed. You can refer to the below links:

[Data flow performance features](https://docs.microsoft.com/sql/integration-services/data-flow/data-flow-performance-features?view=sql-server-ver15)
[Tutorial SSIS performance videos](https://techcommunity.microsoft.com/t5/sql-server-integration-services/tutorial-ssis-performance-videos/ba-p/387581)

## Recommended Steps

- If possible, try executing the package in **64-bit**.
- If SSIS Package is running on the same machine as SQL Server and if SQL Server is consuming most of the memory, reduce the memory cap for SQL Server, or try to execute the SSIS Package on another machine.
- Sometimes third-party components\drivers (for instance some versions of Oracle OLEDB driver) are known to cause memory leak issues. To isolate the issue, remove the third-party components from the package for a test run.

### **Account related issues**

In some cases, a package might run in Visual Studio SSDT and the execution fails post deployment with a different account.

## Recommended Steps

1. Ensure that the package is failing due to permission differences between the two accounts: Execute the package with the same account that was used to execute it on Visual Studio SSDT.
2. If the Package executes successfully under one account and fails under another, then one of the accounts is missing a required privilege. This may be a privilege for a network share for a connection or a privilege on the OS level.

**How to run an SSIS Package under a different account through an SQL Server Agent Job**<br>
For SQL Server Agent Jobs, an SSIS Package can be run by an account other than the SQL Agent Service Account by using a proxy account. Refer to the below documentation to understand the concept of proxies in SQL Agent:

- [Creating a SQL Server Agent Proxy](https://docs.microsoft.com/sql/ssms/agent/create-a-sql-server-agent-proxy?view=sql-server-ver15)
- [Using SQL Server Agent Proxy for an SSIS Package](https://docs.microsoft.com/sql/integration-services/packages/sql-server-agent-jobs-for-packages?view=sql-server-ver15#to-automate-package-execution-by-using-sql-server-agent)
- [Issues with running an SSIS Package using SQL Server Agent Service Account](https://docs.microsoft.com/troubleshoot/sql/integration-services/ssis-package-doesnt-run-when-called-job-step)

### **Connection related issues**

One of the most common issues that prevents an SSIS package from getting executed successfully is the data source connection.

Connection to a data source can fail in validation phase or in execution phase.

## Recommended Steps
If a connection fails in validation phase, there is either a design issue in the package or an connectivity issue to the data source. 

   - If a connection works during the design phase but fails when the package is executed, try to hardcode the connection properties (connection string, username, password etc.) if the connection manager was parameterized to determine if there is an issue with parameterization.

   - Sometimes, it is necessary to determine if one can connect to the data source outside SSIS using the same driver or not.

   - Below we have discussed how one can test connectivity to OLEDB and ODBC data sources outside SSIS.

### Issues with OLEDB Connections

One of the most used connections in SSIS are OLEDB Connections. One can use an OLEDB Source\Destination adapter and connect to any OLEDB data source (for example SQL Server, Microsoft Excel, Oracle DB etc.), provided the required OLEDB Provider is installed on the machine.

### Test connectivity to an OLEDB source

1. Create a new text file and open it in Notepad.
2. Go to **File** > **Save As**.
3. Change the **Save As Type** to **All Files**.
4. Name the file **UDL.udl**, save and close it. 
6. Open the UDL file you just saved.
7. On the first tab, select the **OLEDB Provider** used in the SSIS package in the OLEDB Connection Manager, and select the **Connection** tab.
8. Enter the connection details and **test connection**. <br>
   If the connection fails, there’s an issue with connectivity to the data source.

### Issues with ODBC Connections

Another heavily-used connection type is ODBC Connection. THis can be used to connect to a variety of data sources via their respective ODBC drivers.

### Test connectivity to an ODBC source

  **Note:** Visual Studio SSDT is a 32-bit tool and requires 32-bit drivers to establish connections in design time. During runtime, one can use 64-bit drivers as well.

1. Search for ODBC Data Sources (choose 64-bit or 32-bit depending on whether the package needs to be executed in 32-bit or 64-bit) and open one. 
2. In the **ODBC Data Source Administrator** window, select the **System DSN** tab, and **Add**.
3. Select the driver used within the SSIS package in ODBC Connection and select **Finish**.
4. The following window and options would vary for different drivers. Fill the data source details and **test connection**.<br>
   If the connection fails, there’s an issue with connectivity to the data source.

### Issues with OData Connections

OData does not support MFA and Modern Authentication in Odata Connection Manager.

- [Supported Authentication Types](https://docs.microsoft.com/sql/integration-services/connection-manager/odata-connection-manager?view=sql-server-ver15#connection-manager-authentication)
- If you want to [enforce connections over TLS 1.2](https://techcommunity.microsoft.com/t5/sql-server-support/tls-issue-with-ssis-package-while-accessing-odata-source-like/ba-p/319077)

**Note:** Intermittent connection issues and connection drops in midst of an execution are not covered here. Some probable causes include: a fault in the network, or server performance.

## **Recommended Documents**

- [Required privileges and rights for SQL Server Services](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15#Serv_Perm)
- [The following article discusses a similar issue](https://techcommunity.microsoft.com/t5/sql-server-support/system-componentmodel-win32exception-a-required-privilege-is-not/ba-p/317804)

