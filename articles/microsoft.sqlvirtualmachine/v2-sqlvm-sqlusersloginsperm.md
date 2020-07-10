<properties
	pageTitle="SQL Users, Logins and permissions"
	description="SQL Users, Logins and permissions"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740101"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="afd45269-8fdd-4272-b11b-df7d4d726011"
	ownershipId="AzureData_AzureSQLVM"
/>



# SQL Users, Logins and permissions

**Can I connect to a SQL Server on Azure VM using Azure Active Directory?**
No, at this time, [connecting to SQL Server running on an Azure VM](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?tabs=azure-powershell) is not supported using an Azure Active Directory account. Use a domain Active Directory account instead.

**I forgot sysadmin (sa) password, how do I login to SQL Server Instance?**
For  a VM deployed with SQL Server market place image, the VM administrator account that you initially created when you first deployed the VM, by default, has sysadmin access to SQL instance. 
If you have not removed that administrator account from SQL instance later, you can remote desktop using the original administrator account to access SQL instance. If you have forgotten original VM administrator account password, you can [reset](https://docs.microsoft.com/azure/virtual-machines/troubleshooting/reset-rdp) it.    

You can also enable SQL authentication and set new user and password as sa, if you have not done it already, provided you have [SQL VM resource provider registered](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/sql-vm-resource-provider-register?tabs=azure-cli%2Cbash) with full mode. This can be done 
by opening [SQL virtual machines resource](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/manage-sql-vm-portal#access-the-sql-virtual-machines-resource) and by selecting Security. VM deployed using SQL market place images by default has the resource provider registered with full mode. This will restart SQL Server instance.

Alternatively, you can remote desktop to the VM as an administrator and do the following from command prompt with administrative privilege to add a new account to the default SQL instance as sysadmin. SQL Server will be restarted during this process. Please replace VM_Name, [Domain\login] with appropriate values for your environment.

``` 

NET STOP MSSQLSERVER
NET START MSSQLSERVER /m"SQLCMD" 
sqlcmd -S VM_Name
```
``` SQLCMD

CREATE LOGIN [Domain\login] FROM WINDOWS; 
GO
ALTER SERVER ROLE sysadmin ADD MEMBER [Domain\login];
GO
Exit
```
```

NET STOP MSSQLSERVER
NET START MSSQLSERVER
```


**Why am I getting 'Login failed for user' error 18456?**
Please check the corresponding state number in the error 18456 and take corrective actions as per [this article](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-ver15). For example: state 8 indicates password provided was incorrect.

**I get login failures after SQL AlwaysOn Availability Group (AG) failover**
Make sure that you are using SQL AG listener in the connection string and reaching to the new primary replica. Ensure that login exists in the new replica with appropriate privileges. It is a good idea to transfer logins from the primary replica to the secondary replicas using a process similar to [Method 2 of this article](https://support.microsoft.com/help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server).

**I am able to remotely login to the SQL Server using SQL authentication, but I am unable to logging remotely using windows authentication**
You may additionally see **Cannot generate SSPI context** error. These issues can happen if there is an issue with **Service Principal Name(SPN)**. Please ensure that SQL Server [Service Principal Name (SPN) is registered correctly](https://docs.microsoft.com/sql/database-engine/configure-windows/register-a-service-principal-name-for-kerberos-connections?view=sql-server-ver15) and there are no duplicate/missing SPNs or SPN errors.

You can use Microsoft® Kerberos Configuration Manager to achieve above as follows:
- Download the Microsoft® Kerberos Configuration Manager https://www.microsoft.com/download/details.aspx?id=39046
- You **must log in the SQL Server VM as the domain administrator to run the utility** against the domain controller.
- The tool will not create a shortcut, so you should note the install path; generally it is in : *C:\Program Files\Microsoft\Kerberos Configuration Manager for SQL Server*
- Click on Connect
- Once connected, click on SPN TAB and on the left for the desired SPN, click Fix. After the fix, restart SQL instance and verify if it was able to use the correct SPN.


## **Recommended Documents**

* [Choose an Authentication Mode](https://docs.microsoft.com/sql/relational-databases/security/choose-an-authentication-mode?view=sql-server-ver15)
* [Permissions (Database Engine)](https://docs.microsoft.com/sql/relational-databases/security/permissions-database-engine?view=sql-server-ver15)
* [Connect to a SQL Server Virtual Machine on Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-connect)
* [How to transfer logins and passwords between instances of SQL Server](https://support.microsoft.com/help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server)
* [Configure Login Auditing](https://docs.microsoft.com/sql/ssms/configure-login-auditing-sql-server-management-studio?view=sql-server-ver15)
