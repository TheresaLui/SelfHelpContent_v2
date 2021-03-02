<properties
  pagetitle="Encryption, TDE, Azure Key Vault (AKV)&#xD;"
  description="Encryption - TDE, Always Encrypted, AKV"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740080"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="b35ad0aa-4229-48f0-b3fb-5caf7c8154c7"
  ownershipid="AzureData_AzureSQLVM" />
# Encryption, TDE, Azure Key Vault (AKV)

4 out of 5 customers were able to resolve issues with Encryption, TDE, Azure Key Vault (AKV) by using the following steps. 

## **Recommended Steps** 

- What is the use of TDE, Always Encrypted, Column Level Encryption and Azure Key Vault and how to set up?
  - **Transparent Data Encryption:** TDE is a mechanism for encrypting database files at rest. Because the scope of encryption is per database, you cannot see the data in the database even if the database file is stolen. If there is sensitive data in the database that should not be accessed by the administrator we recommend to **[Set up SQL Server TDE Extensible Key Management by using Azure Key Vault](https://docs.microsoft.com/sql/relational-databases/security/encryption/setup-steps-for-extensible-key-management-using-the-azure-key-vault?view=sql-server-ver15&tabs=portal)**
  - **Column Encryption:** Encrypt a column of data by using symmetric encryption in SQL Server. This is sometimes known as **[column-level encryption, or cell-level encryption](https://docs.microsoft.com/sql/relational-databases/security/encryption/encrypt-a-column-of-data?view=sql-server-ver15)**
  - **Always Encrypted:** Always Encrypted allows clients to encrypt sensitive data inside client applications and never reveal the encryption keys to SQL Server. As a result, Always Encrypted provides a separation between those who own the data and can view it, and those who manage the data but should have no access. **[Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-database-engine?view=sql-server-ver15)** is a mechanism for applications to encrypt column data. **A major difference compared to the Aforementioned TDE** is that the encryption key can be held on the client side and does not need to be
disclosed to SQL Server.



- Common Errors and Failure with Creating Asymmetric Key 

  - **For SQL Server FCI, Databases are stuck in a recovery pending state after a SQL failover**  

    - EKM dll version and build should be same on all Always on Nodes. 
    - Location of EKM dll should be same such as "C:\Program Files\SQL Server Connector for Microsoft Azure Key Vault\Microsoft.AzureKeyVaultService.EKM.dll"
    - If both the above conditions are satisfied then you can export the registry value from following path
      **_[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\SQL Server Cryptographic Provider]_** and import ore create this entry manually on other Always On AG nodes.

   - **Cannot open session for cryptographic provider 'AzureKeyVault_EKM'. Provider error code: 2050.**
 
     It seems there is some mistake we did while following the initial steps due to which you can get this error. Please [follow this steps](https://docs.microsoft.com/sql/relational-databases/security/encryption/setup-steps-for-extensible-key-management-using-the-azure-key-vault?view=sql-server-ver15&tabs=portal
 ) from start correctly to prevent this error.

  - **Key with name 'xxx' does not exist in the provider or access is denied. Provider error code: 2058**
  
    Create a new [registry Key](https://docs.microsoft.com/sql/relational-databases/security/encryption/sql-server-connector-registry-modification?view=sql-server-ver15) _**[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\SQL Server Cryptographic Provider]**_ and add SQL Service Full Control permissions on this key to resolve this. Finally add SQL server service account to local Admin Group.

   - **Cannot open session for cryptographic provider 'AzureKeyVault_EKM_Prov'. Provider error code: 3303**

     - It seems your client key might have expired Alter the credential using below script here Client ID will remain same and only  client key need to be changed in secret part of TSQL query. 
        ```
        ALTER CREDENTIAL credential_name WITH IDENTITY = 'identity_name'  [ , SECRET = 'secret' ]  
        ```
     - Restart SQL Services.


   - **Cannot open session for cryptographic provider 'SQLKeyVault_EKM_Prov'. Provider error code: 3106.**
   
     Make sure you have the [Visual C++ Redistributable Packages for Visual Studio 2013 x64](https://www.microsoft.com/download/details.aspx?id=40784) on your AG nodes in VM. Uninstall the "SQL Server Connector for Microsoft Azure Key Vault" from control panel and [Reinstall](https://www.microsoft.com/download/details.aspx?id=45344). Make sure SQL Service has full permissions on registry and connector path: C:\Program Files\SQL Server Connector for Microsoft Azure Key Vault\ 

  - **When using RSA-HSM key ,Key with name 'akv' does not exist in the provider or access is denied. Provider error code  : 3. 
(Not Supported - Consult EKM Provider for details)** 
   
     The SQL Connector for Azure Key Vault with the fix for RSA-HSM was released (1.0.5.0 (version 15.0.2000.440)) and can be [downloaded from Here](https://www.microsoft.com/download/details.aspx?id=45344)

   - **Cannot find server asymmetric key with Thumbprint on Always On AG**
  
     - Check if thumbprint of asymmetric key in the secondary replica is different from the one in the primary replica using **_select * from sys.asymmetric_keys_**. 
     - If yes, drop the key on secondary replica and recreate the asymmetric key using the same provider key as the primary server. Take a fresh backup and restore the database on secondary.



- Enable TDE on databases which are a part of Availability Groups or Add Encrypted databases to existing Availability groups
   - Please review [How to enable TDE Encryption on a database in an Availability Group](https://techcommunity.microsoft.com/t5/sql-server-support/how-to-enable-tde-encryption-on-a-database-in-an-availability/ba-p/318086)
   - Please review [How to add a TDE encrypted database to an Availability Group](https://techcommunity.microsoft.com/t5/sql-server-support/how-to-add-a-tde-encrypted-database-to-an-availability-group/ba-p/318490)



- What version or edition of SQL Server Supports TDE/Always Encrypted
  You can check [what features are supported under what version/edition of SQL Server here](https://docs.microsoft.com/sql/sql-server/editions-and-components-of-sql-server-2016?view=sql-server-ver15)



- Failed to enable AKV integration from SQL Virtual Machine Resource on AZURE Portal
   -  Make sure you have the [Visual C++ Redistributable Packages for Visual Studio 2013 x64](https://www.microsoft.com/download/details.aspx?id=40784) on your VM
   -  Uninstall the "SQL Server Connector for Microsoft Azure Key Vault" from control panel and [Reinstall](https://www.microsoft.com/download/details.aspx?id=45344)
   - Restart SQL Service and Enable the [AKV integration from SQL Resource](https://docs.microsoft.com/azure/azure-sql/virtual-machines/windows/azure-key-vault-integration-configure#existing-vms)



- I am using TDE EKM with AKV, how can I extend my client secret/AAD Principle which expires/has expired 
   - We need to update the SQL credential with new secrets.   
   - Create a new secret within the registered application in AAD.  
   - On Secondary replica of AG, execute above query to update the credential. 
     ```
     ALTER CREDENTIAL cred_name WITH IDENTITY = 'vault name',SECRET ='Fill Application (Client) ID,Azure App Client ID Secret'
     ```
    - Restart this instance to trigger DB recovery and check if DB is online/synchronized.  Once secondary databases are synchronized, failover secondary AG to this replica
    - Repeat step to alter credential and restart the instance for this failed over node.



- Restore TDE Enabled Database
  To restore a backup encrypted with a TDE protector from Key Vault, make sure that the key is available to the target server. Therefore, we recommend that you keep all the old versions of the TDE protector in key vault, so database backups can be restored. Please [review the process here](https://docs.microsoft.com/azure/azure-sql/database/transparent-data-encryption-byok-overview?view=sql-server-2017#database-backup-and-restore-with-customer-managed-tde
). You might get **401 error** in application log if your client secret is expired. Renew it and alter the credential with new secret to finish the restore successfully.


## **Recommended Documents**

* [Configure Azure Key Vault Integration for SQL Server on Azure Virtual Machines](https://docs.microsoft.com/azure/virtual-machines/windows/sql/virtual-machines-windows-ps-sql-keyvault)
* [Transparent Data Encryption (TDE)](https://docs.microsoft.com/sql/relational-databases/security/encryption/transparent-data-encryption?view=sql-server-ver15)
* [SQL Server Connector Maintenance & Troubleshooting](https://docs.microsoft.com/sql/relational-databases/security/encryption/sql-server-connector-maintenance-troubleshooting?view=sql-server-ver15)
* [Common errors for transparent data encryption with customer-managed keys in Azure Key Vault](https://docs.microsoft.com/sql/relational-databases/security/encryption/troubleshoot-tde?view=azure-sqldw-latest)
* [Extensible Key Management Using Azure Key Vault](https://docs.microsoft.com/sql/relational-databases/security/encryption/extensible-key-management-using-azure-key-vault-sql-server?view=sql-server-2014#ExampleA)
* [Always Encrypted](https://docs.microsoft.com/sql/relational-databases/security/encryption/always-encrypted-database-engine?view=sql-server-ver15)
* [SQL Server Certificates and Asymmetric Keys](https://docs.microsoft.com/sql/relational-databases/security/sql-server-certificates-and-asymmetric-keys?view=sql-server-ver15)
* [Enable Encrypted Connections to the Database Engine](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15)**
* [Always Encrypted with secure enclaves](https://docs.microsoft.com/sql/relational-databases/security/tutorial-getting-started-with-always-encrypted-enclaves?view=sql-server-ver15&viewFallbackFrom=sql-server-ver152)