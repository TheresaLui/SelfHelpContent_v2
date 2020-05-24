<properties
    pageTitle="Autoscale Flapping Detected"
    description="Flapping occurs when autoscale detects a situation where scaling in one direction would trigger a scaling in the opposite direction."
    service="microsoft.azuremonitoring"
    resource="autoscale"
    authors="Andy Stubbs"
    ms.author="anstubbs"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public"
    articleId="3d010d8c-1afe-4407-91c3-c3c99b3d31f9"
    ownershipId="AzureMonitoring_Autoscale"
/>

# Autoscale Flapping Detected

Autoscale has detected a scenario where the autoscale setting did not scale because doing so would have created a situation called “flapping”. Flapping occurs when the act of scaling in one direction would later cause autoscale to scale in the opposite direction because the margin between the two thresholds is too small.
An example of this is the following:
* Increase instances by 1 count when Thread Count >= 600
* Decrease instances by 1 count when Thread Count <= 600

The above scenario would cause autoscale to scale up or down everytime it is executed. So it is prevented by autoscale.

## **Recommended Steps**

Ensure that the maximum and minimum values are different and have an adequate margin between them. If you have a setting that has minimum=2, maximum=2 and the current instance count is 2, no scale action can occur. Keep an adequate margin between the maximum and minimum instance counts, which are inclusive. Autoscale always scales between these limits.

## **Recommended Documents**

* [Autoscale Best Practices](https://docs.microsoft.com/en-us/Azure/azure-monitor/platform/autoscale-best-practices)
