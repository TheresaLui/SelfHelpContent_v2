<properties
  pagetitle="Issue in SSIS Service"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="hecepeda"
  selfhelptype="Generic"
  supporttopicids="32749438"
  resourcetags=""
  productpesids="14745"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="sqlvm-ssis-issue-ssis-service"
  ownershipid="AzureData_AzureSQLVM" />

# **Issue in SSIS Service**

Integration Services - SSIS service (as a Windows service) provides management support for Integration Services package storage and execution. The service does not need to be up and running for successful execution of SSIS packages on the machine.

### **Issues with starting Integration services (SSIS Service)**

Most users were able to resolve their issues with SQL Server Integration services (SSIS service) using the recommended solutions & documents below.

**Error:** "Event ID: 7000- Description: The SQL Server Integration Services service failed to start due to the following error: The service did not respond to the start or control request in a timely fashion."

and

"A timeout was reached (30000 milliseconds) while waiting for the SQL Server Integration Services service to connect."

During any .NET application startup, the .NET Framework application services validates [code access security (CAS)] for Microsoft assemblies, this is done connecting to a server that has a revocation list in internet.

The above error means that the SSIS timeout is lower than the timeout of the connection to the revoke list server. This issue affects to all applications that runs on .NET framework 2.0 and there are several workarounds for this problem.

## **Recommended Steps**

In general, we can disable the certificate checking in the MsDtsSrvr.exe.config file directly, [By default, this setting is in place unless modified explicitly]

1. Edit the **MsDtsSrvr.exe.config** file located in this folder: `C:\Program Files\Microsoft SQL Server\110\DTS\Binn`.<br>
 [NOTE: Path differs with the version of SQL Server, 110 - SQL 2012, 120 - SQL 2014, 130 - SQL 2016, 140 - SQL 2017, 150 - SQL 2019]
2. Add the " **`<generatePublisherEvidence enabled="false">`** within the `<Runtime>` tag
3. Restart the service.

Other available workarounds include:

1. **Increase the default time-out value for the service control manager:**

Modify the registry to increase the default time-out value for the service control manager. To increase this value to 60 seconds, follow these steps:

  1. Select **Start**, click **Run**, type **regedit**, and then click **OK**.
  2. Locate and then click the following registry subkey: `HKEY\_LOCAL\_MACHINE\SYSTEM\CurrentControlSet\Control`
  3. In the right pane, locate the **ServicesPipeTimeout** entry.
  
    Note: If the **ServicesPipeTimeout** entry does not exist, you must create it. To do this, follow these steps:
    1. On the **Edit** menu, point to **New**, and then click **DWORD Value**.
    2. Type **ServicesPipeTimeout**, and then press **ENTER**.

  4. Right-click **ServicesPipeTimeout**, and then click **Modify**.
  5. Select **Decimal**, type **60000**, and then **OK**. This value represents the time in milliseconds before a service time out.
  6. Restart the computer.

2. **Disabling the global checking of the certificated in the machine:**

Disable the global checking of the certificated in the machine following the steps below:

  1. Go to **Start** > **Control Panel** > **Internet Options** > **Advanced**
  3. Uncheck **Check for publisher's certificate revocation**

**These two workarounds are applicable to any .NET Framework based applications/services universally.**

If the above action items do not resolve the issue, verify that the recent .NET Framework updates / patches were applied completely without any issues during the upgrade process.

Check if the .NET Framework version is stable in the machine. If needed, uninstall the recent .NET framework KBs installed.

**Error:**"Configuration system failed to initialize." 

This error can happen when the SSIS service account does not have the required permission to access .NET framework files like machine.config or if the content of machine.config is corrupted.

If you changed the SSIS service account recently, try to revert the SSIS service account to the original service account, or grant the corresponding permissions for the current service account so it can load machine.config file successfully. Refer the below articles for setting us the permissions for SSIS service account.

[Configure Windows Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)

If you suspect that your machine.config file has been corrupted, please take a back-up of your current machine.config file.

Review machine.config and compare it with a machine.config on a good machine to see if any configuration sections are missing. For example, <system.serviceModel>. If we can identify the missing section above, we can copy the section from good machine to the faulty server and start the server or try to replace the machine.config with the file from a good machine and see whether the service can start successfully.

**Error:** "Class not registered (Exception from HRESULT : 0x80040154 (REGDB_E_CLASSNOTREG)"

This error can happen if the specific COM component is not installed properly or if the SSIS service account does not have the necessary permissions to access the system registry entries.

If you changed the SSIS service account recently, try to revert the SSIS service account to the original service account, or grant the corresponding permissions for the current service account to access the necessary system registry keys. Alternatively, you can try to grant the permissions or change the service account to a local admin account to verify it is really due to permissions.

[Configure Windows Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)

If the class is from some external component (e.g. Office Web Component) or if you cannot identify which COM component is missing, try to install the corresponding component again (check whether it is 32bit or 64bit and install accordingly). Alternatively, if the component is within the SSIS component, try a reinstall of the SSIS component and see whether it is helpful.

**Error:**"An attempt was made to load a program with an incorrect format. (Exception from HRESULT: 0x8007000B)"

This error can happen if specific DCOM components is not granted the required permissions or if some DLL used by SSIS is corrupted.

In your windows event view under application logs, if you see any Microsoft-Windows-DistributedCOM event, like _"The application-specific permission settings do not grant Local Launch permission for the COM Server application with CLSID {GUID} and APPID {APPID}"_, please run DCOMCFG (or go to Control Panel -> Component Services -> DCOM Config. Identify the component based on its CLSID and APPID, and grant the corresponding permissions.

If we don't see the DCOM error, or other related error indicating the exact issue, then it is due to some DLL may be corrupt, we need to try reinstalling Integration services again and check if the issue is resolved.

**Errors:** "Could not load file or assembly xxx (DTS components) and Method 'GetComponentInfos' in type. 'Microsoft.SqlServer.Dts.Server.DtsServer' from assembly 'MsDtsSrvr, Version=x.x.xxx.x, Culture=neutral, PublicKeyToken=\&lt;xxx> does not have an implementation" Or
_or_

"The SQL Server Integration Services service requires Integration Services to be installed by one of these editions of SQL Server 2008 R2: Standard, Enterprise, Developer, or Evaluation. To install Integration Services, run SQL Server Setup and select Integration Services."

These errors can occur if we have a corrupted installation of SSIS. Please reinstall Integration services and check if this resolves the issue.

**Errors:**"Access is denied. (Exception from HRESULT: 0x80070005 (E_ACCESSDENIED)) and Unable to load DLL 'msdtssrvrutil': Access is denied. (Exception from HRESULT: 0x80070005 (E_ACCESSDENIED))

The system cannot find the file specified. (Exception from HRESULT: 0x80070002) and Security must be initialized before any interfaces are marshalled or unmarshalled. It cannot be changed once initialized. (Exception from HRESULT: 0x80010119) and External component has thrown an exception.

Could not read key from registry (Exception from HRESULT: 0x80040150"

This error can happen if the SSIS service account doesn't have the necessary permissions to access the system registry entries.

Did you change the SSIS service account recently? If so, try to revert the SSIS service account to the original service account, or grant the corresponding permissions for the current service account to access the necessary system registry keys. Alternatively, you can try to grant the permissions or change the service account to a local admin account to verify it is really due to permissions.

[Configure Windows Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)


### **Issues with connecting to Integration services (SSIS Service)**

**Error:**

```
DTS_E_INVALIDSSISSERVERNAME/0xC00060AB - "Invalid server name "xxx". SSIS service does not support multi-instance, use just server name instead of "server name\instance
```

This error can happen if we provide an incorrect server name when connecting from Integration services from SQL Server Management Studio (SSMS). Integration services (SSIS service) as windows service, is an Instance-unaware services of SQL Server. You would need to provide the machine name of the server where the service is running and not provide ant instance name or port number. Check or review the name used and remove the backward slash (\\) form the service name that was used for connection.

If you need to list down the packages from different SQL Server MSDB instance, then you can modify the **MsDtsSrvr.ini.xml** configuration file to achieve the desired results.

Please follow the items specified under the below article to correctly modify the **MsDtsSrvr.ini.xml** configuration file.

[Configure the service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#configure-the-service)

If you are looking forward to cluster Integration services, then Clustering Integration Services is not recommended because the Integration Services service is not a clustered or cluster-aware service, and does not support failover from one cluster node to another. Therefore, in a clustered environment, Integration Services should be installed and started as a stand-alone service on each node in the cluster.

[Integration Services (SSIS) in a Cluster](https://docs.microsoft.com/sql/integration-services/service/integration-services-ssis-in-a-cluster?view=sql-server-ver15)


**Error:**

```
"RPC Server unavailable"
```

The Integration Services service uses the DCOM protocol. This error can happen when port used by Integration services viz. 135 is blocked by firewall. The Integration Services service uses port 135, and the port cannot be changed. You have to open TCP port 135 for access to the service control manager (SCM).

Refer to the below articles to open the port 135 and resolve this issue.

[Configure the firewall](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#configure-the-firewall)

[Configure a Windows Firewall for Access to the SSIS Service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#configuring-a-windows-firewall)

**Error:**

```
Connecting to the Integration Services service on the computer "XXXX" failed with the following error: "Access is denied."
```

This error can happen when a user without sufficient rights attempts to connect to an instance of Integration Services on a remote server. You would need to grant the user the required set of DCOM permissions to access the Integration services.

Refer to the below articles to resolve this issue.
[Eliminating the "Access Is Denied" Error](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#eliminating-the-access-is-denied-error)

[Grant permissions to the service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#grant-permissions-to-the-service)

**Error:**

```
Connecting to the Integration Services service on the computer "XXXX" failed with the following error: "Class not registered".
```

This error can occur when you try to connect to legacy version of a SQL Server Integration Services service from the current version of the SQL Server tools. To connect directly to an instance of the legacy Integration Services Service, you have to use the version of SQL Server Management Studio (SSMS) aligned with the version of SQL Server on which the Integration Services Service is running.

Refer the below articles for more details.

[Manage the service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#manage-the-service)

### **Issues with configuring Integration services (SSIS Service)**

**Errors:**

```
Failed to retrieve data for this request. (Microsoft.SqlServer.SmoEnum)
```

The SQL Server specified in Integration Services service configuration is not present or is not available. This might occur when there is no default instance of SQL Server on the computer. For more information, see the topic "Configuring the Integration Services Service" in SQL Server 2008 Books Online.

```
Login Timeout Expired
```

An error has occurred while establishing a connection to the server. When connecting to SQL Server 2008, this failure may be caused by the fact that under the default settings SQL Server does not allow remote connections.

```
Named Pipes Provider: Could not open a connection to SQL Server [2]. (MsDtsSvr).
```

The SSIS service internally uses **MsDtsSrvr.ini.xml** configuration file for connecting to the SQL Server instance in which msdb database contains the packages that the Integration Services service will manage. If the **MsDtsSrvr.ini.xml** configuration file is incorrectly configured or doesn't match up to the configuration of the current SQL Server setup that it needs to connect to, then you can get the above list of error message.

Please follow the items specified under the below article to correctly modify the **MsDtsSrvr.ini.xml** configuration file.

[Configure the service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#configure-the-service).

**Error:**

```
The application-specific permission settings do not grant Local Activation permission for the COM Server application with CLSID

{xxxxxxxxxxxxxxxxxxxxxxxxxxxxx}

and APPID

{xxxxxxxxxxxxxxxxxxxxxxxxxxxxx}

to the user NT SERVICE\SQLSERVERAGENT SID (XXXXXXXXXXX) from address LocalHost (Using LRPC) running in the application container Unavailable SID (Unavailable). This security permission can be modified using the Component Services administrative tool.
```

This error can happen if the service account of the SQL Server Agent doesn't have the Integration Services DCOM [Launch and Activation Permissions].

Refer to the below article to fix this issue.

[To grant access to the Integration Services service](https://docs.microsoft.com/sql/integration-services/service/integration-services-service-ssis-service?view=sql-server-ver15#grant-permissions-to-the-service)
