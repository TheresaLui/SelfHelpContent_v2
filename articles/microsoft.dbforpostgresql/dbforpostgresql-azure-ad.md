<properties
    pageTitle="Configure or use Azure Active Directory authentication"
    description="Configure or use Azure Active Directory authentication"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="Bashar-MSFT"
    ms.author="bahusse"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32788701, 32789527"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-azure-ad"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Configure or use Azure Active Directory authentication

Most users are able to resolve issues with connecting with Azure Active Directory by using the following steps.

## **Recommended Steps**

First, ensure that you have configured an Azure AD administrator for your database server. This step is required in order to associate your database to a specific Azure AD tenant, and to allow the initial access using Azure Active Directory credentials.

Before you can connect with Azure AD (except when using the administrator role), you'll need to create the corresponding Postgres roles on your database. Azure AD users or other entities that do not have a Postgres role associated will fail to connect.

When connecting with an Azure AD user, make sure that:

1. You created the user in the database using `CREATE ROLE "user1@yourtenant.onmicrosoft.com" WITH LOGIN IN ROLE azure_ad_user;`. This only works when you're connected as the Azure AD administrator.
2. You retrieve the access token using `az account get-access-token --resource https://ossrdbms-aad.database.windows.net`
3. The access token is used within 5-10 minutes of being issued. Otherwise, you'll get an error message.
4. You pass the access token as the password, and you append `@servername` to the Azure AD username. This will result in two @ symbols in the username.

When connecting with an Azure AD group, verify that:

1. You created the Azure AD group in the database using `CREATE ROLE "GroupName" WITH LOGIN IN ROLE azure_ad_user;`
2. You retrieved an access token for a group member
3. You connect to the database with the `@servername` appended to the group name. For example, `GroupName@servername`.

When connecting with Managed Identity, ensure the following:

1. You are using a User-assigned Managed Identity
2. You associated the Client ID of the Managed Identity using the following steps:
3. 
   ```sql
   SET aad_validate_oids_in_tenant = off;
   CREATE ROLE myapp WITH LOGIN PASSWORD 'CLIENT_ID' IN ROLE azure_ad_user;
   ```
   
3. You retrieve the token from your VM's Managed Identity endpoint, and specifying the `https://ossrdbms-aad.database.windows.net` resource
4. You connect with the specified Postgres role name, and appending `@servername`. For example, `myapp@servername`.

## **Recommended Documents**

* [Use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
* [Connect with Managed Identity to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-connect-with-managed-identity)
* [Using Azure Data Studio and Azure AD for connecting to Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/new-simpler-way-to-sign-in-to-azure-database-for-postgresql/ba-p/1247272)
