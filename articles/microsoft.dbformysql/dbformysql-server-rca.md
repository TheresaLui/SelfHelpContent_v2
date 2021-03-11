<properties
  pagetitle="Azure Database for MySQL Server was down and I need root cause analysis"
  description="Azure Database for MySQL Server was down and I need root cause analysis"
  service="microsoft.dbformysql"
  resource="servers"
  ms.author="jtoland"
  selfhelptype="Generic"
  supporttopicids="32788523"
  resourcetags="servers,databases"
  productpesids="16221"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="a380d2c5-0985-47cd-86a1-374cfcdab9f4"
  ownershipid="AzureData_AzureDatabaseforMySQL" />

# Azure Database for MySQL Server was down and I need root cause analysis

Azure Database for MySQL Server Single Server is a fully managed database service with minimal requirements for database customizations. The Single Server deployment type is designed to handle most database management functions, such as patching, backups, high availability, and security, with minimal user configuration and control. The architecture is optimized to provide 99.99% availability within a single availability zone. Single Server supports the community version of MySQL 5.6, 5.7 and 8.0. The service is in General Availability today in wide variety of Azure regions.

**Note**: For more information, see [High availability in Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-high-availability).

Many users resolve related issues by leveraging the following guidance.

## Quick tips

Azure Database for MySQL might restart for one of many reasons, such as:

* [Planned maintenance](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#what-is-a-planned-maintenance)
* A user has [restarted Azure Database for MySQL server](https://docs.microsoft.com/azure/mysql/howto-restart-server-portal)
* If planned maintenance is not the issue and a user hasn't restarted the MySQL server, there may be an issue with the database node. If this is the case, please file a support ticket for assistance.

**Note**: Consider [setting up alerts](https://techcommunity.microsoft.com/t5/azure-database-for-mysql/get-alerted-when-your-azure-database-for-mysql-server-is-not/ba-p/1996368) to be notified when Azure Database for MySQL is not accessible.

## **Recommended documents**

* [**Planned maintenance?**](https://docs.microsoft.com/azure/mysql/concepts-planned-maintenance-notification#what-is-a-planned-maintenance)
* [Restart Azure Database for MySQL server using Azure portal](https://docs.microsoft.com/azure/mysql/howto-restart-server-portal)
