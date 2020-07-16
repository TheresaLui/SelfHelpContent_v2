<properties
    pageTitle="Autoscale Flapping Detected"
    description="Flapping occurs when the act of scaling down would later cause autoscale to scale up immediately."
    infoBubbleText="Flapping occurs when the act of scaling down would later cause autoscale to scale up immediately."
    service="microsoft.insights"
    resource="autoscale"
    ms.author="anstubbs"
    displayOrder=""
    selfHelpType="diagnostics"
    supportTopicIds="32683737, 32683738, 32683735, 32683736, 32683745"
    resourceTags=""
    productPesIds="15527"
    cloudEnvironments="public, fairfax, mooncake, usnat, ussec"
    articleId="autoscale-flapping-detected"
    diagnosticScenario=""
    ownershipId="AzureMonitoring_Autoscale"
/>

# Autoscale Flapping Detected

Autoscale has detected a scenario where the autoscale setting did not scale because doing so would have created a situation called "flapping". 

## Flapping
<!--issueDescription-->
Flapping occurs when the act of scaling down would later cause autoscale to scale up immediately because the margin between the two metric trigger thresholds is too small, causing undesired thrashing to the resource.
<!--/issueDescription-->

An example of this is the following:
* Increase instances by 1 count when Thread Count >= 600
* Decrease instances by 1 count when Thread Count <= 600

The above scenario would cause autoscale to scale up right after it is scaled down. So it is prevented by autoscale.

## **Recommended Steps**

Ensure that the maximum and minimum values are different and have an adequate margin between them. If you have a setting that has minimum=2, maximum=2 and the current instance count is 2, no scale action can occur. Keep an adequate margin between the maximum and minimum instance counts, which are inclusive. Autoscale always scales between these limits.

## **Recommended Documents**

* [Autoscale Best Practices](https://docs.microsoft.com/Azure/azure-monitor/platform/autoscale-best-practices)
