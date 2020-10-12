<properties
	pageTitle="SQL Certificate Management, SSL and TLS"
	description="SQL Certificate Management, SSL and TLS"
	service="Microsoft.SqlVirtualMachine"
	resource="SqlVirtualMachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740071"
	resourceTags="windowsSQL"
	productPesIds="14745,16342"
	cloudEnvironments="public,fairfax, usnat, ussec, blackforest, mooncake"
	articleId="7acd2ec1-6427-4e46-bd94-d6d9c781ece0"
	ownershipId="AzureData_AzureSQLVM"
/>



# SQL Certificate Management, SSL and TLS

### SSL certificate missing from dropdown in SQL Server Configuration Manager
Please ensure that your certificate meets the [Certificate Requirements](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15#certificate-requirements)

### Issues with TLS 1.2
As per [TLS 1.2 support for Microsoft SQL Server](https://support.microsoft.com/help/3135244/tls-1-2-support-for-microsoft-sql-server), please ensure that:
- Both SQL Server and .NET framework are up-to-date 
- Corrective actions have been followed for the known issues

## **Recommended Documents**
* [How to enable SSL encryption for an instance of SQL Server](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-mi)
* [SQL Server Certificates and Asymmetric Keys](https://docs.microsoft.com/sql/relational-databases/security/sql-server-certificates-and-asymmetric-keys?view=sql-server-ver15)
* [Certificate Management](https://docs.microsoft.com/sql/database-engine/configure-windows/manage-certificates?view=sql-server-ver15)
* [Enable Encrypted Connections to the Database Engine](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15)
