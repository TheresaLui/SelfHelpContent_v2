<properties
    pageTitle="Configure or use Azure Active Directory authentication"
    description="Configure or use Azure Active Directory authentication"
    service="microsoft.dbforpostgresql"
    resource="servers"
    authors="lufittl-msft"
    ms.author="lufittl"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32742678"
    resourceTags="servers, databases"
    productPesIds="16222, 17067"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbforpostgresql-azure-ad"
    ownershipId="AzureData_AzureDatabaseforPostgreSQL"
/>

# Configure or use Azure Active Directory authentication

Most users are able to resolve issues with connecting with Azure Active Directory using the steps below:

## **Recommended Steps**

First, ensure that you have configured an Azure AD administrator for your database server. This step is required in order to associate your database to a specific Azure AD tenant, and allow the initial access using Azure Active Directory credentials.

Before you can connect with Azure AD (except when using the administrator), you will need to create the corresponding Postgres roles on your database. Azure AD users or other entities that do not have a Postgres role associated will fail to connect.

When connecting with an Azure AD user, make sure that:

1. You have created the user in the database using `CREATE ROLE "user1@yourtenant.onmicrosoft.com" WITH LOGIN IN ROLE azure_ad_user;` (this only works when connected as the Azure AD administrator)
2. You are retrieving the access token using `az account get-access-token --resource https://ossrdbms-aad.database.windows.net`
3. The access token is used within 5-10 minutes of being issued (otherwise you will get an error)
4. You are passing the access token as the password, and are appending `@servername` to the Azure AD username (this will result in two `@` symbols in the username)

When connecting with an Azure AD group, verify that:

1. You have created the Azure AD group in the database using `CREATE ROLE "GroupName" WITH LOGIN IN ROLE azure_ad_user;`
2. You have retrieved an access token for a group member
3. You are connecting to the database with the `@servername` appended to the group name (e.g. `GroupName@servername`)

When connecting with Managed Identity, ensure the following:

1. You are using a User-assigned Managed Identity
2. You have associated the Client ID of the Managed Identity using the following steps:
   ```sql
   SET aad_validate_oids_in_tenant = off;
   CREATE ROLE myapp WITH LOGIN PASSWORD 'CLIENT_ID' IN ROLE azure_ad_user;
   ```
3. You are retrieving the token from your VM's Managed Identity endpoint, and specifying the `https://ossrdbms-aad.database.windows.net` resource
4. You are connecting with the specified Postgres role name, and appending `@servername` (e.g. `myapp@servername`)

## **Recommended Documents**

* [Use Azure Active Directory for authenticating with PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-configure-sign-in-aad-authentication)
* [Connect with Managed Identity to Azure Database for PostgreSQL](https://docs.microsoft.com/azure/postgresql/howto-connect-with-managed-identity)
* [Using Azure Data Studio and Azure AD for connecting to Azure Database for PostgreSQL](https://techcommunity.microsoft.com/t5/azure-database-for-postgresql/new-simpler-way-to-sign-in-to-azure-database-for-postgresql/ba-p/1247272)
