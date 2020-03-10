<!-- for "other" support topic -->
<properties
    pageTitle="Blueprint assignment basics"
    description="Blueprint assignment basics"
    service="microsoft.blueprint"
    resource="blueprintAssignments"
    authors="alex-frankel"
    ms.author="alfran"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32613345"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax"
    articleId="6298586f-5b16-441a-a5cd-eb9d8a7f49f0"
	ownershipId="ASEP_ContentService_Placeholder"
/>
# Azure Blueprints - Blueprint assignment basics

Most users are able to resolve their blueprint assignment issue using the steps below

## **Recommended Steps**

**Is your assignment failing unexpectedly?**

* If it is an `Azure Resource Manager Template` artifact, it may not necessarily be a blueprint issue. Consider checking the [ARM template documentation](https://docs.microsoft.com/azure/azure-resource-manager/templates/).
* If it is a permissions issue, make sure the managed identity you are using has the right permissions. The `System Assigned` managed identity will only have permissions on the assigned subscription. [Learn more about the blueprint lifecycle](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages#the-blueprint-assignment-object-is-created).

## **Recommended Documents**

* [Stages of a blueprint assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages)
* [Using parameters with a blueprint](https://docs.microsoft.com/azure/governance/blueprints/concepts/parameters)
* [Deploying blueprints in a specific sequence](https://docs.microsoft.com/azure/governance/blueprints/concepts/sequencing-order)
* [Resource locking in blueprints](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking)
