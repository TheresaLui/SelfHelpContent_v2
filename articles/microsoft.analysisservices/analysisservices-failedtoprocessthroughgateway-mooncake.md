<properties
    pageTitle="Failed to process model with data source through gateway"
    description="Failed to process model with data source through gateway"
    service="microsoft.analysisservices"
    resource="servers"
    authors="brspie"
    ms.author="chanwa"
    displayOrder="3"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
    articleId="cc4f16bb-7b0c-49cc-8041-6c37e9f1b2ce"
    ownershipId="AzureData_AnalysisServices"
/>

# Failed to process model with data source through gateway

## **Recommended Steps**

1. Open the config file **Update with new file name here** under the installation directory of the gateway, typically it's **%systemdrive%\Program Files\On-premises data gateway**.
2. Find the **Send Telemetry** setting in the config and change the value to **False**
3. Restart the gateway service **On-premise data gateway service**
4. If processing continues to fail, please open a [support request](data-blade:Microsoft_Azure_Support.NewSupportRequestBlade) to resolve this issue
