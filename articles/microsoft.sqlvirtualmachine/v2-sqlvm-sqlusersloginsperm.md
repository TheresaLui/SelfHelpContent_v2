<properties
  pagetitle="SQL Users, Logins and permissions"
  description="SQL Users, Logins and permissions"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740101"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="afd45269-8fdd-4272-b11b-df7d4d726011"
  ownershipid="AzureData_AzureSQLVM" />
# SQL Users, Logins and permissions

4 out of 5 customers were able to resolve issues with SQL Logins and Permissions by using the following steps. 

## **Recommended Steps** 

- **Common Login Failed Errors** 
   
   * **Login failure for Microsoft "SQL Server IaaS Agent Query service"** 
     
     Make sure **Microsoft SQL Server IaaS Agent service** is using the **[NT Service\SqlIaaSExtensionQuery](https://techcommunity.microsoft.com/t5/sql-server/sql-server-iaas-extension-query-service-for-sql-server-on-azure/ba-p/386015)** account and the account is added to SQL Server as a login with [SysAdmin Permissions](https://docs.microsoft.com/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out?view=sql-server-ver15#step-by-step-instructions)

  

   * **Can I connect to a SQL Server on Azure VM using Azure Active Directory?**

     No, at this time, [connecting to SQL Server running on an Azure VM](https://techcommunity.microsoft.com/t5/azure/login-to-sql-server-in-virtual-machine-using-azure-active/m-p/1794517) is not supported using an Azure Active Directory account. Use a domain [Active Directory account instead.](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-overview)

  * **Cannot login to SQL Server and I am locked out/Forgot my SA Account Password**

      If you cannot login to SQL Server, please follow [these steps to resolve](https://docs.microsoft.com/sql/database-engine/configure-windows/connect-to-sql-server-when-system-administrators-are-locked-out?view=sql-server-ver15#step-by-step-instructions)

  * **The login is from an untrusted domain and cannot be used with Windows authentication**  
  
      Solution to resolve this is [documented here](https://techcommunity.microsoft.com/t5/sql-server-support/error-message-quot-login-failed-the-login-is-from-an-untrusted/ba-p/317473)
 
   * **I am able to remotely login to the SQL Server using SQL authentication, but I am unable to logging remotely using windows authentication**

     You may additionally see **Cannot generate SSPI context** error. These issues can happen if there is an issue with **Service Principal Name(SPN)**. Please ensure that SQL Server [Service Principal Name (SPN) is registered correctly](https://docs.microsoft.com/sql/database-engine/configure-windows/register-a-service-principal-name-for-kerberos-connections?view=sql-server-ver15) and there are no duplicate/missing SPNs or SPN errors.

- **How can I restrict Access to SQL Server from Specific IP Address only**

   [Create an inbound NSG rule](https://docs.microsoft.com/azure/virtual-network/network-security-groups-overview#security-rules) to access the SQL server on the port you are using with the IP Address

- **Best Practice to Secure your SQL Server**
   - Use non default port for SQL Server and block port 1433.
   - Place SQL Server behind a firewall. Only allow connections from designated sources
   - Control all data access through stored procedures and grant access to those instead of giving blanket db_datareader and db_datawriter permissions to the data itself
   - Set a password on SA account and restrict its use. Also, Change the password periodically
   - Remove BUILTIN/Administrators from the sysadmin role and give sysadmin rights in SQL to specific domain accounts that need it.
   - Use Windows Authentication and Windows Only Mode if possible. Do not run SQL on domain controller.
   - Enable the Failed Login option (Server Properties | Security tab) so can look for failed logins to see if an unauthorized person is trying to access the server.
   - Keep up to date on patches and service packs for the operating system and SQL.
   - Make Sure you have windows firewall/NSG enabled for your SQL VM.
 
## **Recommended Documents** 
* [Troubleshoot 18456 Login failure Error](https://docs.microsoft.com/sql/relational-databases/errors-events/mssqlserver-18456-database-engine-error?view=sql-server-ver15)
* [Choose an Authentication Mode](https://docs.microsoft.com/sql/relational-databases/security/choose-an-authentication-mode?view=sql-server-ver15)
* [Permissions (Database Engine)](https://docs.microsoft.com/sql/relational-databases/security/permissions-database-engine?view=sql-server-ver15)
* [Connect to a SQL Server Virtual Machine on Azure](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-sql-connect)
* [How to transfer logins and passwords between instances of SQL Server](https://support.microsoft.com/help/918992/how-to-transfer-logins-and-passwords-between-instances-of-sql-server)
* [Configure Login Auditing](https://docs.microsoft.com/sql/ssms/configure-login-auditing-sql-server-management-studio?view=sql-server-ver15)
* [Creating Security Groups for SQL Server](https://docs.microsoft.com/windows/security/identity-protection/access-control/active-directory-security-groups#security-groups)