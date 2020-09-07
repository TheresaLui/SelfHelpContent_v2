<properties
    pageTitle="Creating, scaling, and deleting an Azure Database for MySQL server"
    description="Creating, scaling, and deleting an Azure Database for MySQL server"
    service="microsoft.dbformysql"
    resource="servers" 
	authors="Xin-Cheng"
	ms.author="chengxin"
    displayOrder="460"
    selfHelpType="generic"
    supportTopicIds="32684526"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="585C3BAD-C062-42E6-8BA2-7173BE1383B4"
	ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Creating, scaling, and deleting an Azure Database for MySQL server

[!Note]
- **Due to ongoing COVID 19, we have mobilized our global response plan to help customers and partners stay up and running during this critical time. We are actively monitoring performance and usage trends 24/7 to ensure we are optimizing our services for customers worldwide, while accommodating this significant new demand.**

- **We have established clear criteria for prioritizing new cloud capacity if needed – top priority will be going to first responders, health and emergency management services, critical government infrastructure, and ensuring remote workers stay up and running with the core functionality of Teams.**

- **We appreciate that these can raise questions, so we have tried to address the most common ones in our [recent blog post](https://azure.microsoft.com/blog/update-2-on-microsoft-cloud-services-continuity).**

Databases in Azure Database for MySQL servers can be managed through the ARM template, using the Azure CLI and by calling our REST APIs. Note that most of the management operations are asynchronous and you might have to poll the status of the operation when using Azure CLI or REST APIs.

Most users are able to resolve their issue using the steps below.

## **Recommended Steps**

* In Azure Database for MySQL, the [mysql system database](https://dev.mysql.com/doc/refman/8.0/en/system-schema.html) is read-only as it is used to support various PaaS service functionality. Please note that you cannot change anything in the `mysql` system database.
* Charset and collation are the only database properties that are supported in current framework. Please refer to [Supported charset and collation](https://dev.mysql.com/doc/refman/8.0/en/charset-charsets.html) for more information. If you would like to change other properties during database creation or update, connect to MySQL using a client like Azure CLI and execute [CREATE DATABASE](https://dev.mysql.com/doc/refman/8.0/en/creating-database.html) or [ALTER DATABASE](https://dev.mysql.com/doc/refman/8.0/en/alter-database.html).
* To familiarize yourself with using ARM templates to create databases in Azure Database for MySQL server, refer to [Create databases in Azure Database for MySQL](https://github.com/Azure/azure-mysql/tree/master/arm-templates/ExampleWithDatabase) ARM template
* Please note: "Update databases" is not an available option in the ARM Template. Please make sure charset and collation for a database stay the same when you rerun the deployment.
        
* If you are using Azure CLI:

  * Make sure you are signed-in to the correct using **az login**
  * Ensure you are using the correct subscription, in case you have more than one
  * Specify all required parameters in **az mysql server create** with valid values. Consult the [CLI reference documentation](https://docs.microsoft.com/cli/azure/mysql?view=azure-cli-latest) for required parameters and valid values.
  
* Consult the [REST API reference documentation](https://docs.microsoft.com/rest/api/mysql/) if you encounter issues using our REST API

## **Recommended Documents**

* [Azure Database for MySQL servers](https://docs.microsoft.com/azure/mysql/concepts-servers)<br>
* [Supported versions](https://docs.microsoft.com/azure/mysql/concepts-supported-versions)<br>
* [Available pricing tiers](https://docs.microsoft.com/azure/mysql/concepts-pricing-tiers)<br>
* [Current know limitations](https://docs.microsoft.com/azure/mysql/concepts-limits)
