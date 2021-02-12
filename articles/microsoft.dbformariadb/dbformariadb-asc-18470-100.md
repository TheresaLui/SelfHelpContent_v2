<properties
	pageTitle="SSL connection errors"
	description="RCA - SSL connection errors RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformariadb"
	resource="dbformariadb"
	authors="haz"
	ms.author="haz"
	displayOrder="100"
	articleId="dbformariadb-asc-18470-100"
	diagnosticScenario="OrcasMariaDBSSLNotSpecified"
	selfHelpType="rca"
	supportTopicIds="32640117,32640118,32640120"
	resourceTags="windows, linux"
	productPesIds="16617"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>
# Can't connect MariaDB database server because of SSL connection errors

<!--issueDescription-->
During our investigation we determined that connections to your database server are failing because the server was configured to require an SSL connection and connection attempts to the server were made without SSL.
<!--/issueDescription-->

## **Recommended Steps**

1. To fix this issue, please ensure SSL is configured correctly on the server. You can refer to [this article](https://docs.microsoft.com/azure/mariadb/concepts-ssl-connection-security) for assistance with configuring your client applications to connect to Azure Database for MariaDB using SSL.
2. You can also obtain system-generated connection strings for common application libraries by navigating to your database server in the [Azure Portal](https://portal.azure.com) and clicking on the "**Connection Strings**" blade.
3. As a part of our maintenance activity, we are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/mariadb/concepts-ssl-connection-security#default-settings). Refer to the steps to mitigate the issue in [this article](https://docs.microsoft.com/azure/mariadb/concepts-certificate-rotation)

## **Recommended Documents**

* [Azure Database for MariaDB](https://azure.microsoft.com/services/mariadb/)
* [Configure SSL connectivity in your application](https://docs.microsoft.com/azure/mariadb/howto-configure-ssl#enforcing-ssl-connections-in-azure)
* [MariaDB Discussion forum](https://social.msdn.microsoft.com/Forums)
