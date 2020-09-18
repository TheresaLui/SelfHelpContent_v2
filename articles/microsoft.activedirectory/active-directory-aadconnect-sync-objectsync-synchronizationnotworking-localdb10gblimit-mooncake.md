<properties
    pageTitle="Synchronization Service stops working after LocalDB reaches 10-GB limit"
    description="Synchronization Service stops working after LocalDB reaches 10-GB limit"
    service="microsoft.aad"
    resource="Microsoft_AAD_IAM"
    authors="cychua"
    ms.author="cychua"
    displayOrder="52"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags="directory_ad_connect"
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="active-directory-aadconnect-sync-objectsync-synchronizationnotworking-localdb10gblimit-mooncake"
	ownershipId="AzureIdentity_User"
/>

# Synchronization Service stops working after LocalDB reaches 10-GB limit

## **Recommended Steps**

* Azure AD Connect requires a SQL Server database to store identity data. You can either use the default SQL Server 2012 Express LocalDB installed with Azure AD Connect or use your own full SQL. SQL Server Express imposes a 10-GB size limit. When using LocalDB and this limit is reached, Azure AD Connect Synchronization Service can no longer start or synchronize properly.

* To recover from this issue, follow the steps described in article [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit).


## **Recommended Documents**

* [Azure AD Connect: How to recover from LocalDB 10-GB limit](https://docs.azure.cn/active-directory/hybrid/tshoot-connect-recover-from-localdb-10gb-limit)  
