<properties
	pageTitle="SQL Users, Logins and permissions"
	description="SQL Users, Logins and permissions"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740101"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="afd45269-8fdd-4272-b11b-df7d4d726011"
	ownershipId="AzureData_AzureSQLVM"
/>



# SQL Users, Logins and permissions

## **Common Issues**
**Can I connect to a SQL Server on Azure VM using Azure Active Directory?** <br>
>No, at this time, [connecting to SQL Server running on an Azure VM](https://docs.microsoft.com/azure/sql-database/sql-database-aad-authentication-configure?tabs=azure-powershell) is not supported using an Azure Active Directory account. Use a domain Active Directory account instead.

**Why am I getting 'Login failed for user' error 18456** <br>
>Please check the corresponding state number in the error 18456 and take corrective actions as per [this article](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-ver15). Example: state 8 indicates password provided was incorrect.


**I get login failures after SQL AlwaysOn Availability Group (AG) failover** 
>Make sure that you are using SQL Ag listener in the connection string and reaching to the new primary replica
Ensure that login exists in the new replica with appropriate privileges. It is a good idea to transfer logins from the primary replica to the secondary replicas using a process similar to **[Method 2 of this article](https://support.microsoft.com/help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server)**.

**I am able to remotely login to the SQL Server using SQL authentication, but I am unable to logging remotely using windows authentication** <br>
>You may additionally see **Cannot generate SSPI context"** error. These issues can happen if there is an issue with **Service Principal Name(SPN)**. Please ensure that SQL Server [Service Principal Name (SPN) is registered correctly](https://docs.microsoft.com/en-us/sql/database-engine/configure-windows/register-a-service-principal-name-for-kerberos-connections?view=sql-server-ver15) and there is no duplicate/missing SPNs or SPN errors.<br>

You can use Microsoft® Kerberos Configuration Manager to achieve above as follows –
- Download the Microsoft® Kerberos Configuration Manager https://www.microsoft.com/en-us/download/details.aspx?id=39046
- You **must log in the SQL Server VM as the domain administrator to run the utility** against the domain controller.
- The tool will not create a shortcut, so you should note the install path; generally it is in : C:\Program Files\Microsoft\Kerberos Configuration Manager for SQL Server
- Click on Connect
- Click connect 
- Once connect, click on SPN TAB, and on your left, for the desire SPN , click fix. After the fix , restart SQL instance and verify if it was able to use the correct SPN.<br>



## **Recommended Documents**
* [Choose an Authentication Mode](https://docs.microsoft.com/sql/relational-databases/security/choose-an-authentication-mode?view=sql-server-ver15)
* [Permissions (Database Engine)](https://docs.microsoft.com/sql/relational-databases/security/permissions-database-engine?view=sql-server-ver15)
* [Connect to a SQL Server Virtual Machine on Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-connect)
* [How to transfer logins and passwords between instances of SQL Server](https://support.microsoft.com/help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server)
* [Configure Login Auditing](https://docs.microsoft.com/sql/ssms/configure-login-auditing-sql-server-management-studio?view=sql-server-ver15)
