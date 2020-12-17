<properties
    pageTitle="TLS 1.2 Upgrade Documents - TLS < 1.2 without override"
    description="RCA - Documents recommended to for information on upgrading to using TLS 1.2"
    infoBubbleText="The customer is recommended to upgrade to using TLS 1.2"
    service="microsoft.documentdb"
    resource="databaseAccounts"
    authors="tomrlake"
    ms.author="tolake"
    articleId="cosmosdb-tls12-upgrade-current-without-override-rca"
    diagnosticScenario="CosmosDBTLS12Insight"
    selfHelpType="rca"
    supportTopicIds=""
    resourceTags=""
    productPesIds="15585"
    cloudEnvironments="public, fairfax, blackforest, mooncake, usnat, ussec"
    ownershipId="AzureData_AzureCosmosDB"
/>

# TLS 1.2 Upgrade Documents - TLS < 1.2 without override
We see you are using TLS that is less than 1.2. These versions are insecure. 

## Documents on why to switch to TLS 1.2:

* [Preparing for TLS 1.2 in Microsoft Azure](https://azure.microsoft.com/updates/azuretls12/)
* [TLS 1.2 enforcement on Azure Cosmos DB](https://devblogs.microsoft.com/cosmosdb/tls-1-2-enforcement/)
* [Enabling TLS 1.2 with the Windows registry](https://docs.microsoft.com/windows-server/identity/ad-fs/operations/manage-ssl-protocols-in-ad-fs#enable-and-disable-tls-12)

## More information based on SDK used:

* [.NET Framework](https://docs.microsoft.com/dotnet/framework/network-programming/tls)
* [Java](https://www.java.com/en/configure_crypto.html)
* [Python](http://pyfound.blogspot.com/2017/01/time-to-upgrade-your-python-tls-v12.html)
* [Node.js](https://nodejs.org/api/tls.html)
