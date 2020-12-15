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

**Error 40532: Cannot open server {servername} requested by the login. The login failed.**

## **Recommended Steps**

Error 40532 is usually related to one of the following scenarios:

1. **The username (login) contains the '@' symbol (e.g., a login of the form "user@mydomain.com")**  
   If the {servername} value shown in the error is "mydomain.com" then you are encountering this scenario.  See [Handling Error 40532](https://techcommunity.microsoft.com/t5/azure-database-support-blog/providing-the-server-name-explicitly-in-user-names-for-azure-sql/ba-p/368942?WT.mc_id=pid:13491:sid:32745429/) for how to handle this.

1. **The subnet where you are trying to connect from has Microsoft.Sql service endpoint enabled**  

   Turning on virtual network service endpoints to Microsoft.Sql in the subnet enables the endpoints for Azure SQL Database, Azure Synapse Analytics, Azure Database for PostgreSQL server, Azure Database for MySQL server and Azure Database for MariaDB. Attempts to connect from subnet might fail if virtual network rules are not set.

   This issue is usually originated by one of the following:

   - Aiming to connect to SQL Database using service endpoints, Microsoft.Sql was enabled in the subnet but the virtual network rule for the originating subnet in the 'Firewalls and virtual networks' settings on the server was not added.
   - Aiming to connect to other database service (like Azure Database for MySQL as an example), Azure SQL Database was also impacted.  

   To fix this issue [create a virtual network rule in your database in SQL Database](https://docs.microsoft.com/azure/azure-sql/database/vnet-service-endpoint-rule-overview#use-the-portal-to-create-a-virtual-network-rule) for the originating subnet in the 'Firewalls and virtual networks'. You can also consider removing the service endpoint from the subnet, but you will need to take into consideration the impact in all the services mentioned above.