<!-- for "other" support topic -->
<properties
    pageTitle="Other blueprint assignment issues"
    description="Other blueprint assignment issues"
    service="microsoft.blueprint"
    resource="blueprintAssignments"
    authors="alex-frankel"
    ms.author="alfran"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739608"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="6298586f-5b16-441a-a5cd-eb9d8a7f49f0-assignment"
    ownershipId="Compute_AzureBlueprint"
/>

<!-- H1s will not be displayed but are required -->
# Azure Blueprints - Other blueprint assignment issues

Most users are able to resolve their blueprint assignment issue using the steps below.

## **Recommended Steps**

* If your issue is with an `Azure Resource Manager Template` artifact, it may not necessarily be a blueprint issue. Consider checking the [ARM template documentation](https://docs.microsoft.com/azure/azure-resource-manager/templates/).
* If it is a permissions issue, make sure the managed identity you are using has the right permissions. The `System Assigned` managed identity will only have permissions on the assigned subscription. [Learn more about the blueprint lifecycle](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages#the-blueprint-assignment-object-is-created).
* If you need to view the blueprint in more depth, you can export the full JSON of the blueprint definition.
  * [Export via PowerShell](https://docs.microsoft.com/azure/governance/blueprints/how-to/import-export-ps)
  * [Export via REST](https://docs.microsoft.com/rest/api/blueprints/blueprints/get)

### Other possible issues

* Blueprint assignments cannot be cancelled. They will timeout after six hours. With very few exceptions, most assignments should not take this long to deploy.
* Deleting a blueprint assignment will **not** remove the resources that it provisioned. Resources created by the blueprint assignment need to be cleaned up manually.

## **Recommended Documents**

* [Stages of a blueprint assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages)
* [Using parameters with a blueprint](https://docs.microsoft.com/azure/governance/blueprints/concepts/parameters)
* [Deploying blueprints in a specific sequence](https://docs.microsoft.com/azure/governance/blueprints/concepts/sequencing-order)
* [Resource locking in blueprints](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking)
