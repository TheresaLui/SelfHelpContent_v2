<properties
	pageTitle="SSL connection errors"
	description="RCA - SSL connection errors RCA"
	infoBubbleText="Found recent connection failure. See details on the right"
	service="microsoft.dbformysql"
	resource="dbformysql"
	authors="kummanish"
	ms.author="manishku"
	displayOrder="100"
	articleId="dbformysql-asc-18470-100"
	diagnosticScenario="OrcasMySQLSSLNotSpecified"
	selfHelpType="rca"
	supportTopicIds="32628367"
	resourceTags="windows, linux"
	productPesIds="16221"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>
# Can't connect MySQL database server because of SSL connection errors

<!--issueDescription-->
During our investigation we determined that connections to your database server are failing because the server was configured to require an SSL connection and connection attempts to the server were made without SSL.
<!--/issueDescription-->

## **Recommended Steps**

1. To fix this issue, please ensure SSL is configured correctly on the server. You can refer to [this article](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security) for assistance with configuring your client applications to connect to Azure Database for MySQL using SSL. You can download application libraries and connection instructions for many common languages [here](https://docs.microsoft.com/azure/mysql/concepts-connection-libraries).
2. You can also obtain system-generated connection strings for common application libraries by navigating to your database server in the [Azure Portal](https://portal.azure.com) and click on the "**Connection Strings**" blade.
3. As a part of our maintenance activity, we are working on changing out gateway certificate used to [connect to the server using SSL](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security#ssl-default-settings). Refer to the steps to mitigate the issue in [this article](https://docs.microsoft.com/azure/mysql/concepts-certificate-rotation)

## **Recommended Documents**

* [Azure Database for MySQL](https://azure.microsoft.com/services/mysql/)
* [Configure SSL connectivity in your application](https://docs.microsoft.com/azure/mysql/howto-configure-ssl#step-3--enforcing-ssl-connections-in-azure)
* [MySQL Discussion forum](https://social.msdn.microsoft.com/Forums/home?forum=AzureDatabaseforMySQL)
