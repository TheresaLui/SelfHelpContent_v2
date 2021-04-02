<properties
 pageTitle="Solve SQL Server startup issues on a stand-alone server"
 description="Solve SQL Server startup issues on a stand-alone server"
 articleId="12D1A15E-F755-46A3-992F-DC09253C36C8"
 productFamilyId = "7aa8b5ba-4d1a-644d-aeca-bc4decdb15de"
 productPesIds="16907,16899,16893,16887,16881"
 supportTopicIds="32684380"
 ms.author="ramakoni"
 ownershipId="serviceshub"
 selfHelpType="generic"
 cloudEnvironments="public"
/>

# Solve SQL Server startup issues on a stand-alone server

## **Recommended Steps**

Most users are able to resolve their SQL Server startup issues using the following steps and documents. Please scroll down for detailed troubleshooting information about each error.

### Summary

You may receive an error when trying to start SQL server from any of the tools like SQL Server Configuration manager, Windows Service Control manager, SQL Server Management Studio (SSMS) etc. This troubleshooter helps you solve the following startup errors:

- Error 2: The system cannot find the file specified
- Error 5: Access is denied
- Error 13: Windows could not start the SQL Server \<Instance Name> on Local Computer
- Error 1067: The process terminated unexpectedly
- Error 1068: The dependency service or group failed to start
- Error 1069: The service did not start due to a logon failure
- Error 1814: Windows could not start the SQL Server \<Instance Name> on Local Computer
- Error 17113: Windows could not start the SQL Server \<Instance Name> on Local Computer
- Error -2146885628: Windows could not start the SQL Server \<Instance Name> on Local Computer

Please scroll down for detailed troubleshooting information about each error.

> Note:
>
> - The error message may vary slightly depending on the tool that you use. However, in general, the event IDs, error numbers, and descriptions are very similar.
> - All these troubleshooters use Service Control Manager to identify the startup error, and they use SQL Server Configuration Manager to provide a resolution.
> - Troubleshooting typically requires that you are an administrator on the SQL Server computer.
> - For more information on file and registry locations for default and named instances review [File Locations for Default and Named Instances of SQL Server](https://docs.microsoft.com/sql/sql-server/install/file-locations-for-default-and-named-instances-of-sql-server?view=sql-server-ver15)

### Error 2: The system cannot find the file specified

The error can occur when the Microsoft SQL Server binary file (Sqlservr.exe) is either renamed or removed on the system that’s hosting the SQL Server service.  
To fix the issue:

1. Confirm the issue by checking for the presence of Event ID:7000 in the System event log.

1. Resolve the issue by repairing the SQL Server installation per the procedure that's documented in [Repair a Failed SQL Server Installation](https://docs.microsoft.com/sql/database-engine/install-windows/repair-a-failed-sql-server-installation?view=sql-server-ver15).

For more information review [Event ID 7000 and SQL Server doesn't start](https://docs.microsoft.com/troubleshoot/sql/admin/event-id-7000-fail-start).

### Error 5: Access is denied

This error can occur when you configure the Microsoft SQL Server service to run under an account that does not have sufficient privileges on the SQL Server installation folder.

To fix the issue:

1. Check for Event ID: 7000 in the Application event log to confirm the symptom.
1. Using either Microsoft SQL Server Configuration Manager or Service Control Manager, note the service account for SQL Server service.
1. Go to the SQL Server installation folder (default is C:\Program Files\Microsoft SQL Server\MSSQL{nn}.MyInstance), check the Effective Access for the service account under the Security tab in the properties of the folder and remove any Deny permissions that may have been assigned to the service account.

> Note: Replace {nn} with 15 for SQL Server 2019, 14 for SQL Server 2017, 13 for SQL Server 2016, 12 for SQL Server 2014, 11 for SQL server 2012. Replace MyInstance with your instance name.

For more information review ["Access is denied" error and SQL Server doesn't start](https://docs.microsoft.com/troubleshoot/sql/admin/event-id-7000-access-denied)

### Error 13: Windows could not start the SQL Server \<Instancename> on Local Computer

This error can occur either when all the network protocols for a Microsoft SQL Server instance are disabled or when there are invalid characters in the thumb print value of the certificate that is manually provisioned for SQL server service.

To fix the issue:

#### Scenario: All SQL Server protocols are disabled

1. Confirm the symptom by checking for event id:7024 in the System event log and SQL error log for messages indicating that all the protocols are disabled.
1. After you verify the problem that's mentioned in the Symptoms section, use the SQL Server Network Configuration node of SQL Server Configuration Manager to enable the required network protocols. Then, restart the SQL Server service.

For more information review [SQL Server can't start if all the protocols are disabled](https://docs.microsoft.com/troubleshoot/sql/admin/error-17182-protocols-disabled-start-failure)

#### Scenario:Issue with thumb print value in the certificate

1. Confirm the symptom by checking for the presence of event id:33556 in the Application event log.

1. Resolve the issue by using one of the following methods:
   1. Provision certificate by using SQL Server configuration manager:
      1. Remove the thumb print value manually from the registry subkey: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server\MSSQL{nn}.yInstance\MSSQLServer\SuperSocketNetLib\Certificate
      1. Use Configuration Manager to re-provision the certificate and restart SQL Service.
   1. Fix invalid characters in Thumbprint value 1. Right click the certificate in Certificate Snap-in in MMC console and copy the Thumbprint value into a text file. Remove any leading or trailing spaces. 1. Remove the thumb print value manually from the registry subkey: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server\MSSQL{nn}.MyInstance\MSSQLServer\SuperSocketNetLib\Certificate 1. Manually paste the new value, or retype the value that you got from the text file and restart SQL service.
      > Note: Replace {nn} with 15 for SQL Server 2019, 14 for SQL Server 2017, 13 for SQL Server 2016, 12 for SQL Server 2014, 11 for SQL server 2012. Replace MyInstance with your instance name.

### Error 1067: The process terminated unexpectedly

This error can occur when SQL Server service can’t find the path that's configured to create error logs. After confirming the cause of the problem by checking for event ID:17058 in the Application event log, you can take the following steps to resolve the issue:

1. Review the path that's set for the ErrorLog file either by:

   1. Checking the value of parameter that starts with -e in the Startup Parameters tab in SQL Server Configuration Manager or
   1. Checking the value in the registry key: HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Microsoft SQL Server\MSSQL{nn}.MyInstance\MSSQLServer\Parameters\SQLArg1

1. Update the path to a valid location in either of these places and restart SQL service.

> Note: Replace {nn} with 15 for SQL Server 2019, 14 for SQL Server 2017, 13 for SQL Server 2016, 12 for SQL Server 2014, 11 for SQL server 2012. Replace MyInstance with your instance name.

For more information on troubleshooting this issue review [Event ID 17058 and SQL Server doesn't start](https://docs.microsoft.com/troubleshoot/sql/admin/event-id-17058-start-sql-server)

### Error 1068: The dependency service or group failed to start

The error occurs when either of the following conditions is true on the SQL server computer:

1. Netlogon service cannot start on SQL Server computer.
1. SQL service starts before Netlogon service is started.

To fix the issue:  
For condition 1, use Service control manager and change the startup account of SQL Server Service to use the Local system account and restart SQL service.

For condition 2, use Service control manager and change SQL service startup type to either Automatic (Delayed Start) or configure failure options to Restart the Service in the Recovery tab of the service.

For more information review [The SQL Server service and the SQL Server Agent Service fail to start on a stand-alone server](https://docs.microsoft.com/troubleshoot/sql/admin/agent-service-fails-start-stand-alone-server)

### Error 1069: The service did not start due to a logon failure

This problem occurs because there is an issue either with the service account itself or the information that is currently saved for the service account.  
To use this troubleshooter, open the System event log, and note the Event ID and description of the event that’s associated with the failure. Then, use the following information to resolve the problem.

#### Event ID 7041: Logon failure: the user has not been granted the requested logon type at his computer

Verify permissions of SQL Service account and ensure the service account has not been assigned any Deny permissions. For more information review [Troubleshooting event id:7041](https://docs.microsoft.com/troubleshoot/sql/admin/error-password-service-account-changed#event-id-7041-logon-failure-the-user-has-not-been-granted-the-requested-logon-type-at-this-computer)

#### Event ID: 7038:This user can't sign in because this account is currently disabled

- If SQL Server Startup account is a Local User Account on the computer, open Computer Management (compmgmt.msc) and verify that the service account is disabled in Local Users & Groups. If it is disabled, enable the account and restart the SQL Server service.
- If SQL Server Startup account is a Windows Domain Account, check whether the account is disabled in Active Directory Users and Computers. If it is disabled, enable the account, and restart the SQL Server service.

#### Event ID: 7038: The user's password must be changed before signing in

1. If the SQL Server Startup account is a Local User Account on the computer, open Computer Management (compmgmt.msc) and clear the User Must change the password at next logon property for SQL Server Startup Account under Local Users & Groups. Then, select OK, and restart the SQL Server service.
1. If the SQL Server Startup account is a Windows Domain Account, open Active Directory Users and Computers, and then verify that the SQL Server Startup Account has the User Must change the password at next logon property enabled.
1. If the property in step 2 is enabled, you must either clear this option or log in interactively to a Windows client, and then set a new password, then, update the new password for the SQL Server Service by using the SQL Server Configuration Manager tool.

#### Event ID: 7038: The user name or password is incorrect

1. The error message entry indicates that the current login name or password set is incorrect. To verify the same, you can use the Run-As Windows option to open a Windows Command Prompt window, and then provide the same credentials. If that works without any issues, carefully type the credentials in SQL Server Configuration Manager.
1. If step 1 fails and reports the same issue, you must reset the password for the Windows logon. If the SQL Server Startup account is a Local User Account on the computer, open Computer Management (compmgmt.msc), and reset the password of the local user. If the SQL Server Startup account is a Windows Domain Account, open Active Directory Users and Computers, and then change the credentials. After the credentials are updated, return to SQL Server Configuration Manager, enter the same credentials, and then start the service.

Type the correct password in the SQL Server service account on the SQL Server host computer. To do this, follow the procedures from [SCM Services - Change the Password of the Accounts Used.](https://docs.microsoft.com/sql/database-engine/configure-windows/scm-services-change-the-password-of-the-accounts-used?view=sql-server-ver15)

#### Event ID: 7038: The referenced account is currently locked out and may not be logged on to

1. If SQL Server Startup account is a Local User Account on the computer, open Computer Management (compmgmt.msc), and clear the Account is Locked Out checkbox for the SQL Server Startup Account under Local Users & Groups. Then, select OK, and restart the SQL Server service.
1. If SQL Server Startup account is a Windows Domain Account, open Active Directory Users and Computers, and verify that the SQL Server Startup Account has the Account is Locked Out property enabled.
1. If the property in step 2 is enabled, you must clear this option, set a strong password, and use the same credentials for the SQL Server Startup Account configuration by using SQL Server Configuration Manager.

### Error 1814: Windows could not start the SQL Server \<Instancename> on Local Computer

This error can occur when Microsoft SQL Server service can’t create the Tempdb file during startup either because the hard disk that was hosting Tempdb was removed or the drive letter changed for some reason or there are space constraints at OS layer.  
To fix the issue:

1. Confirm the symptoms by checking for presence of event ids 5123, 17204 and 1814 in the Application event log.

1. To resolve the problem, move the Tempdb file to a different location by using the procedure that's mentioned in the Failure Recovery Procedure section of [Move System Databases](https://docs.microsoft.com/sql/relational-databases/databases/move-system-databases?view=sql-server-ver15#Failure).

For more information review [Event ID 1814 and SQL Server doesn't start](https://docs.microsoft.com/troubleshoot/sql/admin/event-id-1814-fail-start)

### Error 17113: Windows could not start the SQL Server \<InstanceName> on Local Computer

This error can occur when SQL server cannot access master database.  
To fix the issue:

1. Check SQL Server error log and verify that the cause is the inaccessibility of the master database.

1. Verify the location of the master.mdf file. If the path is incorrect, fix the path by using one of the following options:

   1. In SQL Server Configuration Manager, open the properties pane of your SQL server instance and on the Startup Parameters tab, select the row that starts with -d in the Existing Parameters section and update the same to reflect the correct value, and restart SQL service.

   1. Update the SQLArg0 value to reflect the correct path of master.mdf file HKLM\Software\Microsoft\MicrosoftSQL Server\MSSQL{nn}.MyInstance hive for your SQL server instance.

1. If the master database does exist but is unusable you can return the database to a usable state by either restoring the master database from a full database backup or by rebuilding the master database.

> Note: Replace {nn} with 15 for SQL Server 2019, 14 for SQL Server 2017, 13 for SQL Server 2016, 12 for SQL Server 2014, 11 for SQL server 2012. Replace MyInstance with your instance name.

For more information, review [Service-specific error 17113 when you start SQL Server service](https://docs.microsoft.com/troubleshoot/sql/admin/error-17113-start-service)

### Error -2146885628: Windows could not start the SQL Server \<InstanceName> on Local Computer

This error can occur when the service account does not have permissions to the certificate that is provisioned in Configuration manager.  
To fix the issue:

1. Confirm that the issue by checking for the presence of events 26010 and 33565 in the Application event log.

1. Using Certificates Snap-in in your MMC console, select the certificate configured for SQL server from the list of available certificates under Local Computer account and grant full permissions to SQL Service account by using All Tasks -> Manage Private Keys option.

For more information review [Event ID 33565 and SQL Server doesn't start after you enable encryption](https://docs.microsoft.com/troubleshoot/sql/admin/event-id-33565-start-sql-server)
