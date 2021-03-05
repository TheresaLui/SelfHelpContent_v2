<properties
  pagetitle="SSIS Issue in Package deployment"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="hecepeda"
  selfhelptype="Generic"
  supporttopicids="32749436"
  resourcetags=""
  productpesids="14745"
  cloudenvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
  disableclouds=""
  articleid="sqlvm-ssis-issue-in-package-deployment"
  ownershipid="AzureData_AzureSQLVM" />

# Issue in Package deployment

Review the following solutions for common errors in package deployment.

### Error: "The path for 'ISServerExec.exe' cannot be found. The operation will now exit.

```
A .NET Framework error occurred during execution of user-defined routine or aggregate 'deploy\_project\_internal':
System.Data.SqlClient.SqlException: The path for `ISServerExec.exe` cannot be found. The operation will now exit."
```

This error crops up because the machine where you are trying to deploy the SSIS Project is not recognizing the install path for **ISServerExec.exe.** You either don't have SSIS installed on that machine, or the setup registry path for ISServerExec.exe doesn't actually contain the executable.

   ```
   HKEY\_LOCAL\_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server\130\SSIS\Setup\DTSPath- '130' is for SQL 2016.
   ```

   Check your version and point it to the path where the ISServerExec.exe is available.

### Error "Project Deployment fails or takes a long time to deploy when you have a large number of packages."
   
This error is not specific to SSIS, but almost all projects developed in SQL Server Data Tools. SSDT is a 32bit application, therefore it is governed by a 2 GB memory limit. When there are large amounts of packages in a Project, it will need to build and deploy all of those projects using that contained memory. Read this article, which talks about this in detail [https://docs.microsoft.com/troubleshoot/aspnet/troubleshoot-outofmemoryexception](https://docs.microsoft.com/troubleshoot/aspnet/troubleshoot-outofmemoryexception)

We recommend that you split up your Projects to make it more manageable. In the interim, you can use the 64bit ISDeploymentWizard.exe application to deploy your projects to get around the memory limitation.

### Error:"The package format was migrated from version 6 to version 8. It must be saved to retain migration changes"

You may encounter this issue if you are trying to deploy an older version of a package developed for a previous version of SSIS. When you opened the `.ispac` file in SSDT or deployed the package onto SSISDB catalog, some components of the package could not be updated due to encryption.

Remember to change the Deployment `TargetServerVersion` to match the version of the SQL Server -SSISDB where you are deploying the SSIS Project. You can also use the `ISDeploymentWizard.exe` application aligned to the version of the target SQL Server to deploy your projects.

### .NET Framework errors

```
A .NET Framework error occurred during execution of user-defined routine or aggregate 'deploy\_project\_internal':
System.TypeInitializationException: The type initializer for 'System.Data.SqlClient.SqlConnection' threw an exception. ---> System.TypeInitializationException: The type initializer for 'System.Data.SqlClient.SqlConnectionFactory' threw an exception. ---> System.TypeInitializationException: The type initializer for 'System.Data.SqlClient.SqlPerformanceCounters' threw an exception. ---> System.Configuration.ConfigurationErrorsException: Configuration system failed to initialize ---> System.Configuration.ConfigurationErrorsException: An error occurred loading a configuration file:_ _Access to the path 'C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config' is denied.(C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config) ---> System.UnauthorizedAccessException: Access to the path 'C:\Windows\Microsoft.NET\Framework64\v4.0.30319\Config\machine.config' is denied.
```

As the error message says, validate that the SQL Server service account has the necessary NTFS permissions to access `machine.config` file.


```
A .NET Framework error occurred during execution of user-defined routine or aggregate 'deploy\_project\_internal':
System.ComponentModel.Win32Exception: A required privilege is not held by the client"
```

_Or_  

```
A .NET Framework error occurred during execution of user-defined routine or aggregate "deploy\_project\_internal
System.ComponentModel.Win32Exception: Access is denied"
```

This is one of the known error messages that occur if the SQL Server or SQL Server Agent service account doesn't have the necessary permissions or privileges on the SQL Server machine.

When you deploy, validate or run any SSIS packages from your SSISDB Catalog, it launches the SSIS runtime executable named `ISSERVEREXEC.exe` which is invoked through a .NET CLR assembly within SSISDB by SQL Server service. This invocation needs extended permissions to launch. If the SQL Server service account doesn't have the necessary permissions, you'll encounter this error message.

Resolution steps includes providing the necessary permissions to the SQL Server service account and/or SQL Server Agent Service account.

## **Recommended Steps**

### Provide the necessary Local policy permissions. 

1. On the SQL Server machine, open the **Run** prompt (Windows + R key) and type `secpol.msc`. Select **OK** to open **Local Security Policy** window.
2. Expand **Local Policies** under **Security Settings** in the left pane and select **User Rights Assignment.**
3. In the right pane, open the following Policies and add the **SQL Server Service account** or **SQL Server Agent service account** under the following policies.
  - **Act as a part of Operating system**
  - **Log on as Service.**
  - **Replace a process-level token.**
  - **Bypass traverse checking**
  - **Adjust memory quotas for a process.**
  - **Impersonate a client after authentication.**

### Set the DCOM permissions

1. On the SQL Server machine, open the **Run** prompt (Windows + R key) and type `dcomcnfg.exe`. Select **OK** to open **Component Services** window.
2. On the left pane, go to **Component Services** > **Computers** > **My Computer** > **DCOM Config** node.
3. Under DCOM Config node, based on the version of the Microsoft SQL Server Integration services installed on the SQL Server, choose the respective **Microsoft SQL Server Integration Services** component.

   - Microsoft SQL Server 2012 – Microsoft SQL Server Integration Services 11.0
   - Microsoft SQL Server 2014 – Microsoft SQL Server Integration Services 12.0
   - Microsoft SQL Server 2016 – Microsoft SQL Server Integration Services 13.0
   - Microsoft SQL Server 2017 – Microsoft SQL Server Integration Services 14.0
   - Microsoft SQL Server 2019 – Microsoft SQL Server Integration Services 15.0

  1. Right-click &amp; choose **Properties** of the Microsoft SQL Server Integration Services 1X.0 component.
  2. Under **Security** Tab,
    * Go to **Launch &amp; Activation Permissions** , choose **Customize** option &amp; click **Edit** button. Add the SQL Server Service account and/or SQL Server Agent service account under them. Give **Allow** permissions for **Local Launch, Remote Launch, Local Activation &amp; Remote Activation** for this account.
    * Go to **Access Permissions** , choose **Customize** option &amp; click **Edit** button. Add the SQL Server Service account and/or SQL Server Agent service account under them. Give **Allow** permissions for **Local Access, Remote Access** for this account.
    * Go to **Configuration Permissions** , choose **Customize** option and select the **Edit** button. Add the SQL Server Service account and/or SQL Server Agent service account under them. Give **Allow** permissions for **Full Control, Read &amp; Special Permissions** for this account.

3. Reboot the SQL Server Machine to post the above changes [MANDATORY – Changes will not come into effect if reboot is not performed]. If the issue still persists, collect a RSOP report to make sure that the SQL Server Service account and/or SQL Server Agent service account is added to the necessary policies as mentioned above and there is no explicit DENY permission set of these accounts at the GPO level.

## **Recommended Documents**

Reference: [Configure Windows Service Accounts and Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/configure-windows-service-accounts-and-permissions?view=sql-server-ver15)

