<properties
    pageTitle="I cannot modify server parameter"
    description="I cannot modify server parameter"
    service="microsoft.dbformysql"
    resource="flexibleServers"
    authors="ambhatna"
    ms.author="ambhatna"
    displayOrder="400"
    selfHelpType="generic"
    supportTopicIds="32747605"
    resourceTags="servers, databases"
    productPesIds="17344"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a692ef43-8a0c-4926-b6da-79f8b396496b"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# I cannot modify server parameter

Azure Database for MySQL Flexible Server allows you to configure parameters at a server level using the Azure portal or the Azure CLI. To review the list of parameters, navigate to the **Server parameters** window in the Azure portal.

## **Recommended Steps**

* If the server parameter you want to update is read-only and you cannot update the value in the Azure portal, you can optionally set the parameter at the connection level using **init_connect**.
    >[!Note]
    > `init_connect` can be used to change parameters that do not require SUPER privilege(s) at the session level. To verify if you can set the parameter using `init_connect`, execute the `set session parameter_name=YOUR_DESIRED_VALUE;` command and if it errors out with **Access denied; you need SUPER privileges(s)** error, then you cannot set the parameter using `init_connect'.
* If a parameter you'd like to configure is read-only and you want to set at a server level, let us know by creating a new request or voting for existing requests in our [feedback forum](https://feedback.azure.com/forums/597982-azure-database-for-mysql)
* If there is a change in the server's parameter value from the portal, sometime the client does not see the parameter changed. In such cases client need to reconnect to take param effect after updating param on portal.
* To prevent data from becoming out of sync and to avoid potential data loss or corruption, some server parameters are locked from being updated when using read replicas (ex. `log_bin_trust_function_creators`,`innodb_file_per_table` are locked on both source and replica). To update one of the locked parameters on the source server, please delete replica servers, update the parameter value on the source, and recreate replicas.
* If the server is in read-only mode, please increase the storage size using the portal.
* The read replicas has **read_only = ON**, and we don't support to change it
* To change the in **read_only** parameter for non read replicas, please increase the storage size using the portal.
* Plugin installation is not supported

## **Recommended Documents**

* [Azure Database for MySQL Flexible Server documentation](https://docs.microsoft.com/azure/mysql/flexible-server)<br>
* [Azure Database for MySQL Pricing Page](https://azure.microsoft.com/pricing/details/mysql/)<br>
* [Pricing calculator](https://azure.microsoft.com/pricing/calculator/?service=mysql/)