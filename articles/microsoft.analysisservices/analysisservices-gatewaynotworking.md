<properties
    pageTitle="On-premises data gateway is not working"
    description="On-premises data gateway is not working"
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="chanwa"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="9d9657b4-4a8a-4dae-b285-5263120ffc10"
    ownershipId="AzureData_AnalysisServices"
/>

# On-premises data gateway is not working

While processing, if you see an error like **Gateway on endpoint 'endpoint uri' is unreachable**, make sure the gateway is configured correctly and it is associated with the AS server.

## **Recommended Steps**

1. Open the **On-premises data gateway** in the on-premises server and sign in, check the name and the region, and make sure the network status is **Connected**
2. Open **System Information** in the on-premises server and check the System Name (hostname)
3. Browse the **On-premises Data Gateway** blade of the AS server in the Azure portal, make sure that **AS Region** is same as the region configured in the **On-premises data gateway**
4. Browse the overview blade of the **On-premises Data Gateway** associated with the AS server, make sure that the **Machine name** is the same as the on-premises server

## **Recommended Documents**

* [Connecting to on-premises data sources with Azure On-premises Data Gateway](https://docs.microsoft.com/azure/analysis-services/analysis-services-gateway)
