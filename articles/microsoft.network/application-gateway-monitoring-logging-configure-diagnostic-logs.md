<properties
    pageTitle="Azure Monitoring and logging - Configure diagnostic logs"
    description="Azure Monitoring and logging - Configure diagnostic logs"
    service="microsoft.network"
    resource="applicationgateways"
    authors="v-miegge"
    ms.author="Mario.Liu"
    selfHelpType="resource"
    supportTopicIds="32786123"
    resourceTags=""
    productPesIds="15922"
    ownershipId="CloudNet_AzureApplicationGateway"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="25dee895-b0d0-4840-814a-ead3966840c5"
/>

# Azure Monitoring and logging - Configure diagnostic logs

You can enable diagnostic logs on Application Gateway to get more information about your application traffic and performance. Application Gateway supports three types of logging as explained in the [documentation](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics):

- Access logs
- Firewall logs
- Performance logs (available only for v1 SKUs, use [performance metrics](https://docs.microsoft.com/azure/application-gateway/application-gateway-metrics#metrics-supported-by-application-gateway-v2-sku) for v2 SKU)
- All metrics

> [!NOTE]
> If you are not able to see logs or metrics of your Application Gateway when they are enabled, check if you have any NSG or UDR on the Application Gateway subnet which is blocking internet access. You can learn more on NSG and UDR requirements for Application Gateway [here](https://docs.microsoft.com/azure/application-gateway/configuration-infrastructure).

## **Recommended Steps**

To configure diagnostic logs on your Application Gateway, please follow these steps:

1. Navigate to the Diagnostic settings blade of your Application Gateway in the [Azure portal](https://portal.azure.com).

2. Select the option **Add diagnostic setting**.

3. Select the logs which you want to collect, and then select the storage location.

4. You can choose between a combination of log analytics workspace, or storage account, or event hub.

5. You can access and analyze logs depending on your chosen destination. Log analytics allows for easy analysis right from the Application Gateway blade.

## **Recommended Documents**

- [Learn how to enable diagnostic logs on Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics)
- [Learn how to analyze diagnostic logs on Log Analytics](https://docs.microsoft.com/azure/application-gateway/log-analytics)
