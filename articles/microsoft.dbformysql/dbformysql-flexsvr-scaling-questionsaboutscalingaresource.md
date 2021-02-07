<properties
  pagetitle="Scaling Azure Database for MySQL Flexible Server&#xD;"
  description="Scaling Azure Database for MySQL Flexible Server"
  service="microsoft.dbformysql"
  resource="flexibleservers"
  ms.author="andrela,jtoland"
  selfhelptype="Generic"
  supporttopicids="32747631"
  resourcetags="servers,databases"
  productpesids="17344"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="3f38dbc0-4389-414c-b27c-6186bbf0bb11"
  ownershipid="AzureData_AzureDatabaseforMySQL" />
# Scaling Azure Database for MySQL Flexible Server

In Azure Database for MySQL Flexible Server, you can scale both compute and storage resources. You can initiate scaling operations from the Azure portal, the Azure CLI, ARM templates, or the REST API.

### Considerations

*Compute*

Scaling between all compute tiers and sizes is supported.

* **Connections are dropped and no new connections can be established while compute tiers or sizes are scaled.**

  Compute tier and size scaling requires a server restart. When new connections cannot be established, the time it takes for the window to display varies, but in most cases, is under a minute. It is recommended that you implement retry logic so that your application can seamlessly reconnect to the MySQL server after the scale operation is completed.

*Storage*

Scaling storage is an online operation that does not require a server restart.

* **Scaling fails with error "Service is temporarily busy and the operation cannot be performed. Please try again later".**

  Try to scale the server again after a few minutes have elapsed.

*Read replicas*

* **Can't scale up the source server when a replica exists, or can't scale down a replica.**

  Before updating the configuration of a source server, update the configuration of the replica to equal or greater values. This action ensures that the replica can keep up with any changes made to the source.

Azure Database for MySQL does not support the Azure Monitor auto-scale feature. However, you can configure auto-scaling using Azure run books and Python. Refer to the blog post [How to auto-scale an Azure Database for MySQL/PostgreSQL instance with Azure run books and Python](https://techcommunity.microsoft.com/t5/Azure-Database-Support-Blog/How-to-auto-scale-an-Azure-Database-for-MySQL-PostgreSQL/ba-p/369177).

## **Recommended documents**

* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)
* [Azure Database for MySQL Flexible Server - Compute and storage](https://docs.microsoft.com/azure/mysql/flexible-server/concepts-compute-storage)
* [Manage Azure Database for MySQL Flexible Server](https://docs.microsoft.com/azure/mysql/flexible-server/how-to-maintenance-portal)
* [Migrate to Azure Database for MySQL using dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore/)