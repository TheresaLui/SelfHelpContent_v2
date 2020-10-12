<properties
    pageTitle="Synchronization Service stops working after LocalDB reaches 10-GB limit"
    description="Synchronization Service stops working after LocalDB reaches 10-GB limit"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    displayOrder="2222"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="public, Fairfax, Mooncake, usnat, ussec"
	articleId="6545c2ae-f913-4591-aed8-3f3e5fc7c9b1"
	ownershipId="AzureIdentity_User"
/>

# Synchronization Service stops working after LocalDB reaches 10-GB limit

## **Recommended steps**
* Azure AD Connect requires a SQL Server database to store identity data. You can either use the default SQL Server 2012 Express LocalDB installed with Azure AD Connect or use your own full SQL. SQL Server Express imposes a 10-GB size limit. When using LocalDB and this limit is reached, Azure AD Connect Synchronization Service can no longer start or synchronize properly.

* To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit).


## **Recommended documents**
* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.microsoft.com/azure/active-directory/connect/active-directory-aadconnect-recover-from-localdb-10gb-limit)  
