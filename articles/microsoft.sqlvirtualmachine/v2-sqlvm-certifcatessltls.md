<properties
  pagetitle="Certificate Management, SSL and TLS&#xD;"
  description="SQL Certificate Management, SSL and TLS"
  service="microsoft.sqlvirtualmachine"
  resource="sqlvirtualmachines"
  ms.author="vadeveka,amamun,ujpat"
  selfhelptype="Generic"
  supporttopicids="32740071"
  resourcetags="windowssql"
  productpesids="14745,16342"
  cloudenvironments="public,fairfax,usnat,ussec,blackforest,mooncake"
  articleid="7acd2ec1-6427-4e46-bd94-d6d9c781ece0"
  ownershipid="AzureData_AzureSQLVM" />
# Certificate Management, SSL and TLS

Most customers are able to resolve issues with SSL and TLS certificates by using the following steps. 

## **Recommended Steps** 

- **Use Encrypt=True, TrustServerCertificate=True when making a connection**
   -  SQL communication can be established if `TrustServerCertificate=True`. In this scenario, connection is encrypted and does not validate certificates on the client side.
   -  TLS encryption can be requested from the server or from the client side.`Encrypt=True` allows the client to request encryption.　In this case, connection is encrypted, even if the server is not configured to require encryption.`TrustServerCertificate` also makes the difference between validating a certificate or not. Therefore, `Encrypt=True; TrustServerCertificate=True` does not validate the certificate on the client side, and the communication is TLS encrypted. 
   - If `Force Encryption` is enabled from SQL Server Configuration Manager (SSCM), encryption is requested from the server side. Therefore, there is no need for client-side requests. However, if you need to trust the server's certificate and not validate, select `Encrypt=True; TrustServerCertificate=True` to connect to SQL Server.
 
 - **Error: "Unable to load user-specified certificate [Cert Hash(sha1) "xxx"]. The server will not accept a connection"**
 
   Ensure that your certificate meets the [Certificate Requirements](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15#certificate-requirements).  

   For the Certificate, make sure we have given enough privileges to the SQL server Service account. (Open `mmc.exe` > **Certificates(Local Computer)** > **Personal** > **Certificates** > **All tasks** > **Manage Private Keys** > **Add the service account**.)

- **Error: "Existing connection between servers forcibly closed by the remote host"**   

   To resolve this, make sure both the client and server involved in a connection have the leading zero fixes for **TLS_DHE installed** as suggested in this [public documentation](https://docs.microsoft.com/troubleshoot/windows-server/identity/apps-forcibly-closed-tls-connection-errors).

-  **SSL certificate missing from dropdown in SQL Server Configuration Manager**

   Ensure that your certificate meets the [Certificate Requirements](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15#certificate-requirements).

- **Error: "A fatal error occurred while creating a TLS client credential"**

  As per [TLS 1.2 support for Microsoft SQL Server](https://support.microsoft.com/help/3135244/tls-1-2-support-for-microsoft-sql-server), ensure that:
  - Both SQL Server and .NET framework are up-to-date 
  - Corrective actions have been followed for known issues. [Enable TLS 1.2 on the site servers and remote site systems](https://docs.microsoft.com/mem/configmgr/core/plan-design/security/enable-tls-1-2-server)

- **Connecting to SQL Server on Azure VM Using Azure Active Directory**

   Connecting to a SQL Server instance that's running on an Azure virtual machine (VM) is [not supported using an Azure Active Directory account](https://docs.microsoft.com/azure/azure-sql/database/authentication-aad-overview). Use a domain Active Directory account instead. 

## **Recommended Documents** 

* [Enable Encrypted Connections to the Database Engine](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15)
* [Create your Self Signed Certificate](https://docs.microsoft.com/powershell/module/pkiclient/new-selfsignedcertificate?view=win10-ps)
* [How to enable SSL encryption for an instance of SQL Server](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-mi)
* [SQL Server Certificates and Asymmetric Keys](https://docs.microsoft.com/sql/relational-databases/security/sql-server-certificates-and-asymmetric-keys?view=sql-server-ver15)
* [Certificate Management](https://docs.microsoft.com/sql/database-engine/configure-windows/manage-certificates?view=sql-server-ver15)
* [Changes to hashing algorithm for self-signed certificate in SQL Server 2017](https://techcommunity.microsoft.com/t5/sql-server-support/changes-to-hashing-algorithm-for-self-signed-certificate-in-sql/ba-p/319026)
* [Using Encryption Without Validation](https://docs.microsoft.com/sql/relational-databases/native-client/features/using-encryption-without-validation?view=sql-server-ver15)
