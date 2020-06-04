<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL server"
    description="Creating, scaling, and deleting an Azure Database for MySQL server"
    service="microsoft.dbformysql"
    resource="servers"
    authors="jan-eng"
    ms.author="janeng"
    displayOrder="200"
    selfHelpType="generic"
    supportTopicIds="32640089"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="6b738e5d-8e6e-4fd3-be60-3522d8a20e4a"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL server

[!Note]
- **Due to ongoing COVID 19, we have mobilized our global response plan to help customers and partners stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating this significant new demand.**

- **We have established clear criteria for prioritizing new cloud capacity if needed – top priority will be going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality of Teams.**

- **We appreciate that these can raise questions, so we have tried to address the most common ones in our [recent blog post](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity).**


Azure Database for MySQL servers can be managed through the Azure portal, using the Azure CLI, and by calling our REST APIs. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* In Azure Database for MySQL, the [mysql system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only as it is used to support various PaaS service functionality. Please note that you cannot change anything in the `mysql` system database.
* Make sure that the server name is globally unique
* Currently, minor and major version upgrades aren't supported. For example, upgrading from MySQL 5.6 to MySQL 5.7 isn't supported. If you'd like to upgrade from 5.6 to 5.7, take a [dump and restore](https://docs.microsoft.com/azure/mysql/concepts-migrate-dump-restore) it to a server that was created with the new engine version.
* If you are using the portal, review the [Manage an Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-create-manage-server-portal) how-to

* If you are using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mysql server create** with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
  
* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) if you encounter issues using our REST

## **Recommended Documents**

* [Azure Database for MySQL servers](https://docs.microsoft.com/azure/mysql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)<br>
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Current know limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
