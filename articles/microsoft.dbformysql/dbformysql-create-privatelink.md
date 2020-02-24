<properties
    pageTitle="Create Private link in Azure Database for MySQL"  
    description="Create Private link in Azure Database for MySQL"
    service="microsoft.dbformysql"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32640097"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="6106f5323-5814-4de1-bf80-bb4178aea670"
/>

# Managing Private link in Azure Database for MySQL

Private Link allows you to connect to various PaaS services in Azure via a private endpoint. Azure Private Link essentially brings Azure services inside your private Virtual Network (VNet). The PaaS resources can be accessed using the private IP address just like any other resource in the VNet.

## **Recommended Steps**

* Ensure that the Azure Database for MySQL uses the General Purpose or Memory optimized tier. The Basic tier does not support Private link.
* If you are using the portal, review the [Configure a Private link using Portal](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-portal) how-to
* If you are using the Azure CLI, review the [Configure a Private link using Azure CLI](https://docs.microsoft.com/azure/mysql/howto-configure-privatelink-cli) how-to

## **Recommended Documents**

* [Use Private Link for Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/concepts-data-access-security-private-link)
