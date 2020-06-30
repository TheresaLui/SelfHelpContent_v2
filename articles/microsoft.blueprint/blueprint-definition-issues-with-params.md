<!-- for "other" support topic -->
<properties
    pageTitle="Issues with parameters"
    description="Blueprint definition issues with parameters"
    service="microsoft.blueprint"
    resource="blueprintDefinitions"
    authors="apclouds"
    ms.author="angperez"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739605"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="6298586f-5b16-441a-a5cd-eb9d8a7f49f0-blueprint-definition-issues-with-params"
    ownershipId="Compute_AzureBlueprint"
/>

# Azure Blueprints - Blueprint definition issues with parameters

Blueprint definitions supports parameters at the blueprint level and at the artifacts level. Parameters at the blueprint definition level are known as static parameters, and they can be created through the REST API, Portal, Powershell, and CLI. Static parameters can also be leveraged by the artifacts within the blueprint.

## **Recommended Steps**

Identify what kind of parameters you want to specify at the blueprint level (static parameter) and which ones you want to specify at the artifact level:

* [Blueprint parameter types](https://docs.microsoft.com/azure/governance/blueprints/concepts/parameters)
* [How to create and use static parameters](https://docs.microsoft.com/azure/governance/blueprints/concepts/parameters#blueprint-level-parameter)

## **Recommended Documents**
### What is an Azure blueprint?
* [Azure blueprint overview video](https://docs.microsoft.com/azure/governance/blueprints/overview#video-overview)
### Creating a blueprint
* [Create a blueprint using Azure Portal](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-portal)
* [Create a blueprint using Powershell](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-powershell)
* [Create a blueprint using REST API](https://docs.microsoft.com/azure/governance/blueprints/create-blueprint-rest-api)
* [Create a blueprint using ARM Template](https://docs.microsoft.com/azure/azure-resource-manager/templates/deploy-to-subscription??toc=/azure/governance/blueprints/toc.json&bc=/azure/governance/blueprints/breadcrumb/toc.json)
### Life cycle of a blueprint
* [Life cycle of a blueprint definition and assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/lifecycle)
* [Deploying blueprints in a specific sequence](https://docs.microsoft.com/azure/governance/blueprints/concepts/sequencing-order)
* [Stages of a blueprint assignment](https://docs.microsoft.com/azure/governance/blueprints/concepts/deployment-stages)
