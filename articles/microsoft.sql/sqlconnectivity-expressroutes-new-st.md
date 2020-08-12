<properties
    pageTitle="How to questions: ExpressRoute"
    description="How to questions: ExpressRoute"
    service="microsoft.sql"
    resource="servers"
    authors="VMMicrosoft,subbu-kandhaswamy"
    ms.author="vimahadi,subbuk"
    displayOrder="1"
    selfHelpType="generic"
    supportTopicIds="32745432"
    productPesIds="13491"
    cloudEnvironments="public,blackForest,fairfax, usnat, ussec, mooncake"
    resourceTags="servers, databases"
    articleId="5548CDF8-E853-44CA-9D02-35AE8944C981"
    ownershipId="AzureData_AzureSQLDB_Availability"
/>

# Express Route for Azure SQL Database



* **ExpressRoute** supports using Microsoft peering with route filters for Azure PaaS services, such as Azure storage and Azure SQL Database. You now need only one routing domain to access Microsoft PaaS and SaaS services. You can use route filters to selectively advertise the PaaS service prefixes for Azure regions you want to consume.

* If you are using public peering and currently have IP Network rules for public IP addresses that are used to access Azure Storage or Azure SQL Database, you need to make sure that the NAT IP pool configured with Microsoft peering is included in the list of public IP addresses for the Azure storage account or Azure SQL account.

## **Recommended Documents**
For more information, please visit [Supported services](https://docs.microsoft.com/azure/expressroute/expressroute-faqs?WT.mc_id=pid:13491:sid:32745432/#supported-services) <br>
