<properties
    pageTitle="Manual scaling"
    description="Manual scaling"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="40"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e50-5c75862cc1f1"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783373"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Manual scaling

## **Recommended Steps**

If the performance of your Application Gateway is not optimal or if there is a higher latency than expected, it might be because your gateway instances are stressed due to high traffic. To fix this, you'll need to scale out (increase the number of instances). Your Application Gateway can scale out or scale, in either manually or by autoscaling. Manual scaling is supported both in Application Gateway v1 SKU (Standard/WAF) and v2 SKU (Standard_v2/WAF_v2).

It's important to scale your Application Gateway according to your traffic and with a bit of a buffer, so that you're prepared for any traffic surges or spikes and can minimize the impact on your QoS. In manual scaling, you can manually increase the number of instances of your Application Gateway. To scale out manually, follow the steps below:

1. Navigate to your Application Gateway and select the **Configuration** tab.
2. Choose **Manual** as the capacity type (v2). V1 SKU only supports manual scaling.
3. Under **instance count**, use the slider to set your desired instance count, and then select **Save**.

The number of instances required depends on your traffic workload and peak usage data. To learn how to determine the required number of instances in manual scaling, see [Application Gateway high traffic support](https://docs.microsoft.com/azure/application-gateway/high-traffic-support).

## **Recommended Documents**

- [Autoscaling and Zone-redundant Application Gateway v2](https://docs.microsoft.com/azure/application-gateway/application-gateway-autoscaling-zone-redundant#autoscaling-and-high-availability)
- [Monitoring and alerts for Application Gateway](https://docs.microsoft.com/azure/application-gateway/high-traffic-support#monitoring-and-alerting)
