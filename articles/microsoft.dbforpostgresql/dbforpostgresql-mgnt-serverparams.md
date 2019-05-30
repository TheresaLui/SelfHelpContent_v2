<properties
	pageTitle="Managing server parameters in Azure Database for PostgreSQL"
	description="Managing server parameters in Azure Database for PostgreSQL"
	service="microsoft.dbforpostgresql"
	resource="servers"
	authors="jan-eng"
    ms.author="janeng"
	displayOrder="26"
	selfHelpType="resource"
	supportTopicIds="32639997"
	resourceTags="servers, databases"
	productPesIds="16222"
	cloudEnvironments="public"
	articleId="20c07169-4446-40d0-8323-32ed595cb129"
/>

# Managing server parameters in Azure Database for PostgreSQL

Azure Database for PostgreSQL allows you to configure engine parameters using the Azure portal and Azure CLI. To review the current list of supported parameters, navigate to the **Server parameters** blade in the Azure portal.

**Issue**: An error occurred updating shared_preload_libraries.

   There is a known issue in the portal where updating shared_preload_libraries causes an error. For example, "The value **'TIMESCALEDB'** for configuration 'shared_preload_libraries' is not valid."

   Use the Azure CLI instead to update shared_preload_libraries. 

   ```
   az postgres server configuration set --resource-group myresourcegroup --server mydemoserver --name shared_preload_libraries --value timescaledb
   ```

   You can access the Azure CLI from the Azure portal using Cloud Shell. See the icon toolbar in the top right corner of your screen.

   We apologize for the inconvenience and are working to resolve the portal issue.

## **Recommended Documents**

* [Configure parameters using the Azure portal](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-portal)<br>
* [Configure parameters using the Azure CLI](https://docs.microsoft.com/azure/postgresql/howto-configure-server-parameters-using-cli)
