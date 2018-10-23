<properties
    pageTitle="I can't create an ExpressRoute circuit"
    description="I can't create an ExpressRoute circuit"
    service="microsoft.network"
    resource="expressroutecircuits"
    authors="kasparks"
    displayOrder="6"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="MoonCake"
/>

# I can't create an ExpressRoute circuit

## **Recommended steps**

To resolve the most common issues, try one or more of the following methods.

1. Review [Audit logs](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter) to determine the reason of failure.
2. Check if you are hitting the subscription limits and if it is the reason for not able to create the circuit.<br>
[Check default subscription limits for ExpressRoute resources.](https://docs.azure.cn/azure-subscription-service-limits#networking-limits)
3. Check your subscription permissions to make sure you're allowed to create resources in the region you want the ExpressRoute circuit.

## **Recommended documents**

* [For additional details, see following ExpressRoute Troubleshooting document](https://docs.azure.cn/expressroute/)