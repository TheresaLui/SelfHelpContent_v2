<properties
    pageTitle="Traffic Manager is directing requests to disabled endpoint"
    description="Traffic Manager is directing requests to disabled endpoint"
    service="microsoft.network"
    resource="trafficmanagerprofiles"
    authors="radwiv"
    ms.author="radwiv"
    displayOrder="17"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
	articleId="2171b93f-6cc9-41cf-b88c-f40a0510c0b6"
	ownershipId="CloudNet_TrafficManager"
/>

# Traffic Manager is directing requests to a disabled endpoint

## **Recommended Steps**

1. Cached response might be the reason for directing requests to disabled endpoint. Setting Time to Live (TTL) to a lower value may resolve this issue. A lower TTL lets cached entries expire faster but this may result in more requests to the Traffic Manager service. The default TTL value is 60 seconds, but can be set to a minimum of 0 seconds.

## **Recommended Documents**

* [Traffic Manager Endpoints](https://docs.azure.cn/traffic-manager/traffic-manager-endpoint-types)
* [Traffic Manager Endpoint Monitoring and Failover](https://docs.azure.cn/traffic-manager/traffic-manager-monitoring)
