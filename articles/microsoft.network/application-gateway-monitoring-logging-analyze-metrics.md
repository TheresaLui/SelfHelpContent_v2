<properties
    pageTitle="Azure monitoring and logging - analyze metrics"
    description="Azure monitoring and logging - analyze metrics"
    service="microsoft.network"
    resource="applicationgateways"
    authors="v-miegge"
    ms.author="Mario.Liu"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32786122"
    resourceTags=""
    productPesIds="15922"
    ownershipId="CloudNet_AzureApplicationGateway"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="f8af2728-4c35-410f-ab95-e0fc1b0dd034"
/>

# Azure monitoring and logging - analyze metrics

**Application Gateway** publishes data points, called **metrics**, to [Azure Monitor](https://docs.microsoft.com/azure/azure-monitor/overview) for the performance of your Application Gateway and back-end servers.

Metrics are published in 60-second intervals and are, by default, enabled for your Application Gateway. You can view the metrics directly from the [Azure portal](https://portal.azure.com), or you can stream the values as logs to your storage account, log analytics, or event hub.

**Note:** If you're not able to see the logs or metrics of your Application Gateway when they are enabled, check whether you have any network security groups (NSGs) or user-defined routes (UDRs) on the Application Gateway subnet. NSGs and UDRs can block internet access. You can learn more about NSG and UDR requirements for Application Gateway at [Application Gateway infrastructure configuration](https://docs.microsoft.com/azure/application-gateway/configuration-infrastructure).

## **Recommended Steps**

To analyze metrics, use the following steps:

1. Navigate to the metrics blade of your Application Gateway.

2. You can limit the scope to a single Application Gateway, or you can extend it to multiple gateways to analyze them at the same time.

3. Select the metric that you want to view, as well as the type of chart. You can choose the time range and the granularity, as well.

4. You can apply splitting to metrics, based on the supported dimensions, to get a more filtered view of the data.

## **Recommended Documents**

- [How to enable diagnostic logs for metrics on Application Gateway](https://docs.microsoft.com/azure/application-gateway/application-gateway-diagnostics)
- [Metrics offered by Application Gateway v1 and v2 SKUs](https://docs.microsoft.com/azure/application-gateway/application-gateway-metrics)
