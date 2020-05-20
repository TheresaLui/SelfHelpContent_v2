<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MariaDB server"
    description="Creating, scaling, and deleting an Azure Database for MariaDB server"
    service="microsoft.dbformariadb"
    resource="servers"
	authors="Xin-Cheng"
	ms.author="chengxin"
    displayOrder="430"
    selfHelpType="generic"
    supportTopicIds="32684525"
    resourceTags="servers, databases"
    productPesIds="16617" 
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="D2A141B5-9E23-47A4-A8EE-7314AA4A4D51"
	ownershipId="AzureData_AzureDatabaseforMariaDB"
/>

# Creating, scaling, and deleting an Azure Database for MariaDB server

[!Note]
- **Due to ongoing COVID 19, we have mobilized our global response plan to help customers and partners stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating this significant new demand.**

- **We have established clear criteria for prioritizing new cloud capacity if needed – top priority will be going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality of Teams.**

- **We appreciate that these can raise questions, so we have tried to address the most common ones in our [recent blog post](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity).**


Databases in Azure Database for MariaDB servers can be managed through the ARM template, using the Azure CLI and by calling our REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* In Azure Database for MariaDB, the [mysql system database](https://mariadb.com/kb/en/the-mysql-database-tables/) is read-only as it is used to support various PaaS service functionality. Please note that you cannot change anything in the `mysql` system database.
* Charset and collation are the only database properties that are supported in current framework. Please refer to [Supported charset and collation](https://mariadb.com/kb/en/library/supported-character-sets-and-collations/) for more information. If you would like to change other properties during database creation or update, connect to MariaDB using a client like Azure CLI and execute [CREATE DATABASE](https://mariadb.com/kb/en/library/create-database/) or [ALTER DATABASE](https://mariadb.com/kb/en/library/alter-database/).
* To familiarize yourself with using ARM templates to create databases in Azure Database for MariaDB server, refer to [Create databases in Azure Database for MariaDB](https://github.com/Azure/azure-mariadb/tree/master/arm-templates/ExampleWithDatabase) ARM template
* Please note: "Update databases" is not an available option in the ARM Template. Please make sure charset and collation for a database stay the same when you rerun the deployment.
        
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
