<properties
    pageTitle="How to migrate Azure AD Connect from LocalDB to full SQL"
    description="How to migrate Azure AD Connect from LocalDB to full SQL"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="54"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-howtomigratelocaldbtosql-mooncake"
	ownershipId="AzureIdentity_User"
/>

# How to migrate Azure AD Connect from LocalDB to full SQL

## **Recommended Steps**

You cannot directly replace the LocalDB of an existing Azure AD Connect deployment with the database of the full version of SQL. Instead, you must deploy a new Azure AD Connect server with the full version of SQL. It is recommended that you do a swing migration where the new Azure AD Connect server (with SQL DB) is deployed as a staging server, next to the existing Azure AD Connect server (with LocalDB). 

* For instruction on how to configure remote SQL with Azure AD Connect, refer to article [Custom installation of Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/how-to-connect-install-custom).

* For instructions on swing migration for Azure AD Connect upgrade, refer to article [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.azure.cn/active-directory/hybrid/how-to-upgrade-previous-version#swing-migration).

## **Recommended Documents**

* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit)  
* [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.azure.cn/active-directory/hybrid/how-to-upgrade-previous-version#swing-migration)  
* [Custom installation of Azure AD Connect](https://docs.azure.cn/active-directory/hybrid/how-to-connect-install-custom)  
