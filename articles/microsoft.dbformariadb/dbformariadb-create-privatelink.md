<properties
    pageTitle="Create Private link in Azure Database for MariaDB"  
    description="Create Private link in Azure Database for MariaDB"
    service="microsoft.dbformariadb"
    resource="servers"
    authors="kummanish"
    ms.author="manishku"
    displayOrder="220"
    selfHelpType="generic"
    supportTopicIds="32640897"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public"
    articleId="3b3f555a-e522-4486-bf1f-b222b2d56575"
/>

# Managing Private link in Azure Database for MariaDB

Private Link allows you to connect to various PaaS services in Azure via a private endpoint. Azure Private Link essentially brings Azure services inside your private Virtual Network (VNet). The PaaS resources can be accessed using the private IP address just like any other resource in the VNet.

## **Recommended Steps**

* Ensure that the Azure Database for MariaDB uses the General Purpose or Memory optimized tier. The Basic tier does not support Private link.
* If you are using the portal, review the [Configure a Private link using Portal](https://docs.microsoft.com/azure/mariadb/howto-configure-privatelink-portal) how-to
* If you are using the Azure CLI, review the [Configure a Private link using Azure CLI](https://docs.microsoft.com/azure/mariadb/howto-configure-privatelink-cli) how-to

## **Recommended Documents**

* [Use Private Link for Azure Database for MariaDB](https://docs.microsoft.com/azure/mariadb/concepts-data-access-security-private-link)
