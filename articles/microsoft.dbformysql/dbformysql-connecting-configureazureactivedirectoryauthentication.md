<properties
    pageTitle="Configure or use Azure Active Directory authentication with Azure Database for MySQL Single Server"
    description="Configure or use Azure Active Directory authentication with Azure Database for MySQL Single Server"
    service="microsoft.dbformysql"
    resource="servers"
    ms.author="jtoland"
    selfhelptype="Generic"
    supporttopicids="32788508"
    resourcetags="servers,databases"
    productpesids="16221"
    cloudenvironments="public,fairfax,usnat,ussec"
    articleid="3c60939c-63d0-4b01-b138-ab28df263044"
    ownershipId="AzureData_AzureDatabaseforMySQL"
/>

# Configure or use Azure Active Directory authentication

Azure Database for MySQL Single Server supports authentication with Azure Active Directory Azure AD). Many users resolve related issues by leveraging the following guidance.

## Fix it yourself

To associate your database with a specific Azure AD tenant and to allow the initial access using Azure AD credentials, if you haven't already, configure an Azure AD administrator for your database server.

Aside from the administrator, Azure AD users without an associated MySQL user cannot connect.

When connecting with an Azure AD user, verify that:

1. You connect as the Azure AD administrator and create the user in the database by using the following command:

   `CREATE AADUSER 'user1@yourtenant.onmicrosoft.com';`

2. You're retrieving the access token by using the following command:

   `az account get-access-token --resource https://ossrdbms-aad.database.windows.net`

3. The access token is used within 5-10 minutes of being issued (or you'll encounter an error).
4. You are passing the access token as the password and appending `@servername` to the Azure AD username (resulting in a username with `@` symbols).

When connecting with an Azure AD group, verify that:

1. You've created the Azure AD group in the database using the following command:

   `CREATE AADUSER 'GroupName';`

2. You've retrieved an access token for a group member.
3. You're connecting to the database with `@servername` appended to the group name (e.g., `GroupName@servername`).

When connecting with Managed Identity, verify that:

1. You're using a User-assigned Managed Identity.
2. You've associated the Client ID of the Managed Identity by using the following command:

   ```sql
   SET aad_auth_validate_oids_in_tenant = OFF;
   CREATE AADUSER 'myuser' IDENTIFIED BY 'CLIENT_ID';
   ```

3. You're retrieving the token from your VM's Managed Identity endpoint and specifying the `https://ossrdbms-aad.database.windows.net` resource.
4. You're connecting with the specified MySQL user name and appending `@servername` (e.g., `myapp@servername`).

## **Recommended documents**

* [Use Azure Active Directory for authenticating with Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-configure-sign-in-azure-ad-authentication)
* [Connect with Managed Identity to Azure Database for MySQL Single Server](https://docs.microsoft.com/azure/mysql/howto-connect-with-managed-identity)
