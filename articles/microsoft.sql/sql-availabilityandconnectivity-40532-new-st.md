<properties
    pageTitle="Cannot open server requested by the login"
    description="Cannot open server requested by the login"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745429"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="3A2EF1AF-EC78-47A6-898B-4EA904F08D2A"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Cannot open server requested by the login

Follow these steps to resolve the error, "Error 40532: Cannot open server {servername} requested by the login. The login failed."

## **Recommended Steps**

This error is usually related to one of the following scenarios:

1. **The login username is an email address or contains the '@' symbol (e.g., user@mydomain.com)**  
   If the *servername* value shown in the error is "mydomain.com," you are encountering this scenario. For instructions on how to handle this, see [Handling Error 40532](https://techcommunity.microsoft.com/t5/azure-database-support-blog/providing-the-server-name-explicitly-in-user-names-for-azure-sql/ba-p/368942?WT.mc_id=pid:13491:sid:32745429/).

1. **The subnet from which you are trying to connect has Microsoft.Sql service endpoint enabled**  

   By enabling virtual network service endpoints to Microsoft.Sql in the subnet, you also enable endpoints for Azure SQL Database, Azure Synapse Analytics, Azure Database for PostgreSQL server, Azure Database for MySQL server and Azure Database for MariaDB. Attempts to connect from subnet might fail if virtual network rules are not set.

   This issue usually originates from one of the following actions:

   - When attempting to connect to SQL Database using service endpoints, Microsoft.Sql was enabled in the subnet. However, the virtual network rule for the originating subnet in the **Firewalls and virtual networks** settings on the server was not added.
   - When attempting to connect to other database service (like Azure Database for MySQL as an example), Azure SQL Database was also impacted.  

   To resolve this issue [create a virtual network rule in your database in SQL Database](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#use-the-portal-to-create-a-virtual-network-rule) for the originating subnet in the **Firewalls and virtual networks**. If you remove the service endpoint from the subnet, make sure to consider the impact in all the services mentioned previously.
