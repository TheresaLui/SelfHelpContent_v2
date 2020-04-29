<properties
	pageTitle="SQL Certificate Management, SSL and TLS"
	description="SQL Certificate Management, SSL and TLS"
	service="microsoft.compute"
	resource="virtualmachines"
	ms.author="ujpat,vadeveka,amamun"	
	authors="ujpat,vadeveka,AbdullahMSFT"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32740071"
	resourceTags="windowsSQL"
	productPesIds="14745"
	cloudEnvironments="Public, BlackForest, Fairfax, MoonCake, USSEC, USNAT"
	articleId="7acd2ec1-6427-4e46-bd94-d6d9c781ece0"
	ownershipId="AzureData_AzureSQLVM"
/>



# SQL Certificate Management, SSL and TLS

**Common Issues**
* **SSL certificate missing from dropdown in SQL Server Configuration Manager** <br>
Please ensure that your certificate meets the [Certificate Requirements](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15#certificate-requirements)
 <br>
* **I am having issues with TLS 1.2**  
Please ensure as per [TLS 1.2 support for Microsoft SQL Server](https://support.microsoft.com/help/3135244/tls-1-2-support-for-microsoft-sql-server)
    - that both SQL Server and operating system .Net framework is updated 
    - that you have followed the corrective actions for the know issues

## **Recommended Documents**
* [How to enable SSL encryption for an instance of SQL Server](https://support.microsoft.com/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-mi)
* [SQL Server Certificates and Asymmetric Keys](https://docs.microsoft.com/sql/relational-databases/security/sql-server-certificates-and-asymmetric-keys?view=sql-server-ver15)
* [Certificate Management](https://docs.microsoft.com/sql/database-engine/configure-windows/manage-certificates?view=sql-server-ver15)
* [Enable Encrypted Connections to the Database Engine](https://docs.microsoft.com/sql/database-engine/configure-windows/enable-encrypted-connections-to-the-database-engine?view=sql-server-ver15)