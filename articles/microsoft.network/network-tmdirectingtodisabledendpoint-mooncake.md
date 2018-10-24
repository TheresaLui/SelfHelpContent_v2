<properties
    pageTitle="Traffic Manager is directing requests to disabled endpoint"
    description="Traffic Manager is directing requests to disabled endpoint"
    service="microsoft.network"
    resource="trafficmanagerprofiles"
    authors="radwiv"
    displayOrder="17"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# Traffic Manager is directing requests to disabled endpoint

## **Recommended steps**

1. Cached response might be the reason for directing requests to disabled endpoint. Setting Time to Live (TTL) to a lower value may resolve this issue. A lower TTL lets cached entries expire faster but this may result in more requests to the Traffic Manager service. <br>The default TTL value is 60 seconds which can be set to a minimum of 0 seconds.

## **Recommended documents**

* [Traffic Manager Endpoints](https://docs.azure.cn/traffic-manager/traffic-manager-endpoint-types)
* [Traffic Manager Endpoint Monitoring and Failover](https://docs.azure.cn/traffic-manager/traffic-manager-monitoring)