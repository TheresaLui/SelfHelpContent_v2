<properties
    pageTitle="Configure or use Azure Active Directory authentication"
    description="Configure or use Azure Active Directory authentication"
    service="microsoft.dbformysql"
    resource="servers"
    authors="lufittl-msft"
    ms.author="lufittl"
    displayOrder="30"
    selfHelpType="generic"
    supportTopicIds="32742677"
    resourceTags="servers, databases"
    productPesIds="16221"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="dbformysql-azure-ad"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Configure or use Azure Active Directory authentication

**Note:** **These steps apply when using Active directory with Azure Database for MySQL - Single Server. Flexible Server (Preview) currently does not support Active directory.**

Most users are able to resolve issues with connecting with Azure Active Directory using the steps below:

## **Recommended Steps**

First, ensure that you have configured an Azure AD administrator for your database server. This step is required in order to associate your database to a specific Azure AD tenant, and allow the initial access using Azure Active Directory credentials.

Before you can connect with Azure AD (except when using the administrator), you will need to create the corresponding MySQL users on your database. Azure AD users or other entities that do not have a MySQL user associated will fail to connect.

When connecting with an Azure AD user, make sure that:

1. You have created the user in the database using `CREATE AADUSER 'user1@yourtenant.onmicrosoft.com';` (this only works when connected as the Azure AD administrator)
2. You are retrieving the access token using `az account get-access-token --resource https://ossrdbms-aad.database.windows.net`
3. The access token is used within 5-10 minutes of being issued (otherwise you will get an error)
4. You are passing the access token as the password, and are appending `@servername` to the Azure AD username (this will result in two `@` symbols in the username)

When connecting with an Azure AD group, verify that:

1. You have created the Azure AD group in the database using `CREATE AADUSER 'GroupName';`
2. You have retrieved an access token for a group member
3. You are connecting to the database with the `@servername` appended to the group name (e.g. `GroupName@servername`)

When connecting with Managed Identity, ensure the following:

1. You are using a User-assigned Managed Identity
2. You have associated the Client ID of the Managed Identity using the following steps:
   
   ```sql
   SET aad_auth_validate_oids_in_tenant = OFF;
   CREATE AADUSER 'myuser' IDENTIFIED BY 'CLIENT_ID';
   ```
   
3. You are retrieving the token from your VM's Managed Identity endpoint, and specifying the `https://ossrdbms-aad.database.windows.net` resource
4. You are connecting with the specified MySQL user name, and appending `@servername` (e.g. `myapp@servername`)

## **Recommended Documents**

* [Use Azure Active Directory for authenticating with MySQL](https://docs.microsoft.com/azure/mysql/howto-configure-sign-in-azure-ad-authentication)
* [Connect with Managed Identity to Azure Database for MySQL](https://docs.microsoft.com/azure/mysql/howto-connect-with-managed-identity)
