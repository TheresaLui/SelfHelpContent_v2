<properties
    pageTitle="How to migrate Azure AD Connect from LocalDB to full SQL"
    description="How to migrate Azure AD Connect from LocalDB to full SQL"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="2221"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="c8217076-9f5e-465a-bedd-9c78f79bdf79"
	ownershipId="AzureIdentity_User"
/>

# How to migrate Azure AD Connect from LocalDB to full SQL

## **Recommended steps**
You cannot directly replace the LocalDB of an existing Azure AD Connect deployment with the database of the full version of SQL. Instead, you must deploy a new Azure AD Connect server with the full version of SQL. It is recommended that you do a swing migration where the new Azure AD Connect server (with SQL DB) is deployed as a staging server, next to the existing Azure AD Connect server (with LocalDB). 

* For instruction on how to configure remote SQL with Azure AD Connect, refer to article [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom).

* For instructions on swing migration for Azure AD Connect upgrade, refer to article [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-upgrade-previous-version#swing-migration).

## **Recommended documents**
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
* [Azure AD Connect: Upgrade from a previous version to the latest](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-upgrade-previous-version#swing-migration)  
* [Custom installation of Azure AD Connect](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-get-started-custom)  
