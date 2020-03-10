
<properties
    pageTitle="Moving Log Analytics Workspace"
    description="Moving Log Analytics Workspace"
    service="microsoft.operationsmanagement"
    resource="solutions"
    authors="dougbrad"
    ms.author="dougbrad"
    displayorder="1"
    selfHelpType="resource"
    supportTopicIds=""
    resourceTags=""
    productPesIds=""
    cloudEnvironments="public, Blackforest, Fairfax"
	articleId="f032d0fa-1e51-4441-ba1d-8c8bcb0f2125"
	ownershipId="ASEP_ContentService_Placeholder"
/>

# Moving Log Analytics Workspace

## **Recommended Steps**

If you need to move your Log Analytics Workspace to another subscription or resource group, please follow the steps below:

1. Delete the Solutions that are enabled on the Workspace
2. Move the Workspace to the new Subscription/Resource Group
3. Add the Solutions again

If this is not followed, the solutions may remain in the old location and dashboards in a non-working state, possibly requiring a request to support to fix this issue.
