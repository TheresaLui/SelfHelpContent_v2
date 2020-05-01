<properties
    pageTitle="Other blueprint assignment issues"
    description="Other blueprint assignment issues"
    service="microsoft.blueprint"
    resource="blueprintAssignments"
    authors="alex-frankel"
    ms.author="alfran"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32739606"
    resourceTags=""
    productPesIds="16600"
    cloudEnvironments="public, fairfax"
    articleId="managed-identity-and-other-permissions-issues"
    ownershipId="Compute_AzureBlueprint"
/>

<!-- H1s will not be displayed but are required -->
# Azure Blueprints - Managed identity and other permissions issues

Most users are able to resolve their blueprint assignment issue using the steps below.

## **Recommended Steps**

* There are two types of **managed identities** that you can choose between when assigning a blueprint:
  * **System assigned**: This identity gets owner rights only on the assigned subscription. It requires that the user or principal assigning the blueprint **also has owner permissions on the subscription**. It is automatically created for you. When the blueprint assignment is deleted, the system-assigned managed identity will also be deleted.
    * This identity will be deleted in when the blueprint assignment is deleted.
  * **User assigned**: This is a managed identity resource that is created separately from the blueprint assignment. By default a new managed identity won't have any permissions in Azure. It is up to you (or another administrator at your organization) to configure the permissions. This is required if the blueprint needs to perform actions outside the scope of the assigned subscription.
    * This identity will have an exemption to any blueprint locks (deny assignments), so be aware of other services using this identity.
* The system assigned managed identity **only has owner permissions on the assigned subscription**, which means any cross-subscription actions (e.g. VNET peering or accessing a key vault) will fail. To make sure you have the necessary permissions, you will need to use a user-assigned managed identity with access to all resources that are required to complete the blueprint assignment.