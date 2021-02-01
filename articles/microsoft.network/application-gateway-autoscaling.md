<properties
    pageTitle="Autoscaling"
    description="Autoscaling"
    service="microsoft.network"
    resource="applicationgateways"
    authors="TobyTu"
    ms.author="mariliu"
    displayOrder="41"
    selfHelpType="resource"
    articleId="7640a487-6f9f-4a3c-9e50-5c75862cc1f2"
    resourceTags=""
    productPesIds="15922"
    supportTopicIds="32783374"
    cloudEnvironments="public,fairfax,mooncake,blackforest,ussec,usnat"
    ownershipId="CloudNet_AzureApplicationGateway"
/>

# Autoscaling

## **Recommended Steps**

If the performance of your Application Gateway is not optimal or if there is a higher latency than expected, it might be because your gateway instances are stressed due to high traffic, and you'll need to scale out (increase the number of instances). Your Application Gateway can scale out or scale in, either manually or autoscaling.

Autoscaling is available only in v2 SKU (Standard_v2/WAF_v2). It is important that you scale your Application Gateway according to your traffic, and with a bit of a buffer. This way, you're prepared for any traffic surges or spikes, and you're minimizing the impact that spikes or surges have in your QoS.

Follow these steps to enable autoscaling:

1. Navigate to your Application Gateway and select the **Configuration** tab.
2. Choose **Autoscale** in the capacity type.
3. Under **minimum instance count**, use the slider to set the minimum instance count you want, and then select **Save**.

    **Note:** This is the count of number of instances that will always be running, and your Application Gateway's instance count will not go below this number. It's best to set this number to a higher value than what's needed, in order to provide a 20 percent buffer to handle any short spikes or bursts in traffic.

4. Under **maximum instance count**, use the slider and set your maximum instance count.

    Make sure that your Application Gateway subnet has enough IP addresses available to support this number. Otherwise, you'll have to re-create your gateway in the same or different subnet which has enough capacity.

The minimum and maximum number of instances required depends on your traffic workload and peak usage data. To learn how to determine the required number of instances in manual scaling, see [Application Gateway high traffic support](https://docs.microsoft.com/azure/application-gateway/high-traffic-support).

## **Recommended Documents**

- [Autoscaling for Application Gateway v2 SKU (Standard_v2/WAF_v2 SKU)](https://docs.microsoft.com/azure/application-gateway/high-traffic-support#autoscaling-for-application-gateway-v2-sku-standard_v2waf_v2-sku)
- [Autoscaling and Zone-redundant Application Gateway v2](https://docs.microsoft.com/azure/application-gateway/application-gateway-autoscaling-zone-redundant#autoscaling-and-high-availability)
- [Monitoring and alerts for Application Gateway](https://docs.microsoft.com/azure/application-gateway/high-traffic-support#monitoring-and-alerting)
