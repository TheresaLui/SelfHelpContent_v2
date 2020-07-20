<properties
    pageTitle="Blueprint locks issues"
    description="Blueprint locks issues"
    service="microsoft.blueprint"
    resource="blueprintAssignments"
    authors="alex-frankel"
    ms.author="alfran"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739603"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="blueprint-locks-issues"
    ownershipId="Compute_AzureBlueprint"
/>

# Azure Blueprints - Blueprint lock issues

## **Recommended Steps**

* The `managed identity` you choose will automatically get an exemption to the blueprint lock so that it can continue to manage resources in the blueprint
* You can exempt up to four additional principals from the blueprint lock with the `excludedPrincipals` property. [Learn how to exempt principals from a blueprint assignment here](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking#exclude-a-principal-from-a-deny-assignment)
* You can exempt specific actions with the `excludedActions` property. For example, even with a `ReadOnly` lock, you may still want to allow for a VM restart action. [Learn how to exempt actions from a blueprint assignment here](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking#exclude-an-action-from-a-deny-assignment)
* A `denyAssignment` can **only** be created by either the Azure Blueprints or Azure Managed Applications services. You can view active deny assignments in the IAM blade of the relevant scopes and resources, but they cannot be created, updated or deleted except via the whitelisted services.

## **Recommended Documents**

* [General overview of blueprint locks](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking)
* [Tutorial on creating a blueprint with locks](https://docs.microsoft.com/azure/governance/blueprints/concepts/resource-locking)
* [General overview of Deny Assignments](https://docs.microsoft.com/azure/role-based-access-control/deny-assignments)
