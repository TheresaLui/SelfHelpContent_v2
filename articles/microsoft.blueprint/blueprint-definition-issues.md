<!-- for "other" support topic -->
<properties
    pageTitle="Other blueprint definition issues"
    description="Other blueprint definition issues"
    service="microsoft.blueprint"
    resource="blueprintAssignments"
    authors="alex-frankel"
    ms.author="alfran"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739609"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="6298586f-5b16-441a-a5cd-eb9d8a7f49f0"
    ownershipId="Compute_AzureBlueprint"
/>

# Azure Blueprints - Other blueprint definition issues

Most users are able to resolve their blueprint definition issue using the steps below.

## **Recommended Steps**

* Blueprint definitions only support a limited set of functions. Only a small set of ARM Template functions are supported in the blueprint definition. You can still use ARM Template functions inside of an ARM Template artifact. [View the full list of Blueprint functions here](https://docs.microsoft.com/azure/governance/blueprints/reference/blueprint-functions).
* Blueprint definitions must be published with a distinct version before they can be assigned to a subscription. [Follow the Blueprints Portal QuickStart for a detailed walk through](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-portal).
* Blueprints can be assigned via [Portal](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-portal), [PowerShell](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-powershell), or [REST API](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-rest-api). PowerShell assignment supports a parameters file to avoid manually filling out a long list of parameters in the portal.

## **Recommended Documents**

* [Using built-in blueprints](https://docs.microsoft.com/azure/governance/blueprints/tutorials/create-from-sample)
* [Lifecycle of a blueprint definition and assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/lifecycle)
* [Deploying blueprints in a specific sequence](https://docs.microsoft.com/azure/governance/blueprints/concepts/sequencing-order)
* [Stages of a blueprint assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages)
