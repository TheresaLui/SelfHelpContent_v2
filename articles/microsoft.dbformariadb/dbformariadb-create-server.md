<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MariaDB server"
    description="Creating, scaling, and deleting an Azure Database for MariaDB server"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="ajlam"
    ms.author="andrela"
    displayOrder="200"
    selfHelpType="generic"
    supportTopicIds="32640151"
    resourceTags="servers, databases"
    productPesIds="16617"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="1844b470-2ee8-423b-8e7c-31202a0b5a99"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Creating, scaling, and deleting an Azure Database for MariaDB server

[!Note]
- **Due to ongoing COVID 19, we have mobilized our global response plan to help customers and partners stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating this significant new demand.**

- **We have established clear criteria for prioritizing new cloud capacity if needed – top priority will be going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality of Teams.**

- **We appreciate that these can raise questions, so we have tried to address the most common ones in our [recent blog post](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity).**


Azure Database for MariaDB servers can be managed through the Azure portal, using the Azure CLI, and by calling our REST APIs. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* In Azure Database for MariaDB, the [mysql system database](https://mariadb.com/kb/en/the-mysql-database-tables/) is read-only as it is used to support various PaaS service functionality. Please note that you cannot change anything in the `mysql` system database.
* Make sure that the server name is globally unique
* Currently, minor and major version upgrades aren't supported. For example, upgrading from MariaDB 10.2 to MariaDB 10.3 isn't supported. If you'd like to upgrade from 10.2 to 10.3, take a [dump and restore](https://docs.microsoft.com/azure/mariadb/howto-migrate-dump-restore) it to a server that was created with the new engine version
* If you are using the portal, review the [Manage an Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/tutorial-design-database-using-portal) tutorial
* If you are using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mariadb server create** with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mariadb?view=azure-cli-latest) for required parameters and valid values.

* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mariadb/) if you encounter issues using our REST

## **Recommended Documents**

* [Azure Database for MariaDB servers](https://docs.microsoft.com/azure/mariadb/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mariadb/concepts-supported-versions)<br>
* [Available pricing tiers](https://docs.microsoft.com/azure/mariadb/concepts-pricing-tiers)<br>
* [Current know limitations](https://docs.microsoft.com/azure/mariadb/concepts-limits)
