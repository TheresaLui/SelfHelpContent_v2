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
    cloudEnvironments="public"
    articleId="1844b470-2ee8-423b-8e7c-31202a0b5a99"
/>

# Creating, scaling, and deleting an Azure Database for MariaDB server

Azure Database for MariaDB servers can be managed through the Azure portal, using the Azure CLI, and by calling our REST APIs. All management operations are supported in each of the options. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* Make sure that the server name is globally unique
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
