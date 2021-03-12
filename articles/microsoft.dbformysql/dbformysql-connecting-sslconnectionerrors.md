<properties
  pagetitle="Azure Database for MySQL SSL/TLS connection errors"
  description="Azure Database for MySQL SSL/TLS connection errors"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788525"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a73901b7-dc2d-48a8-bcc5-af4a6ffc5cfb"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Azure Database for MySQL SSL/TLS connection errors

Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

* Ensure that you’re using the correct [SSL configuration](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security) and the right certificate. Also, be sure that you [Configure SSL connectivity in your application to securely connect to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-ssl).

**Note**: As a part of our maintenance activity, we’re working on [changing the root certificate for the client application/driver enabled with SSL](https://docs.microsoft.com/azure/mysql/concepts-certificate-rotation).

* Ensure that you’re using the correct TLS configuration. To configure TLS for Single Server, see [TLS configuration](https://docs.microsoft.com/azure/mysql/howto-tls-configurations).

  **Note**: If you use the Flexible Server deployment mode, TLS/SSL is enabled by default and can’t be disabled. The minimum TLS version supported on the server is TLS 1.2. All incoming connections with TLS 1.0 and TLS 1.1 will be denied. You can't disable or change the TLS version.

## Quick tips

* It's highly recommended that you only use supported [drivers and tools](https://docs.microsoft.com/azure/mysql/concepts-compatibility) and the latest version of the client.

## **Recommended documents**

* [Configure SSL connectivity in your application to securely connect to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-ssl)
* [Drivers and tools](https://docs.microsoft.com/azure/mysql/concepts-compatibility)
* [SSL configuration](https://docs.microsoft.com/azure/mysql/concepts-ssl-connection-security)
* [Changing the root certificate for the client application/driver enabled with SSL](https://docs.microsoft.com/azure/mysql/concepts-certificate-rotation)
