<properties
    pageTitle="Azure Boards Permissions"
    description="Permissions for work items, queries, and boards"
    infoBubbleText="Azure Boards permissions"
    service="microsoft.visualstudio"
    resource="account"
    authors="danhellem"
    ms.author="dahellem"
    articleId="AZDevOpsBoardsPermissions"
    supportTopicIds="32453004"
    diagnosticScenario=""
    selfHelpType="generic"
    resourceTags=""
    productPesIds="15543"
    cloudEnvironments="public"
    ownershipId="Azure_DevOps_Services"
/>

# Work Item Permission Issues

## **Recommended Steps**

Are you facing one of these common problems?

* I am unable to access a board or backlogs

  - Check to make sure you have permissions to the team backlog or board. [Learn more](https://docs.microsoft.com/azure/devops/boards/get-started/permissions-access-boards?view=azure-devops)

* I am unable to save a work item

  - Check to make sure you have permissions to the project, area path, and iteration path you are saving the work item too. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops)

* I can't assign a work item to a specific person

  - If you attempt to assign a work item to a person who has never logged into the project, you may get an error. The resolve this, have the person log into the project. This will sync the AAD identity into Azure DevOps

* I am not able to move a work item from one project to another

  - This usually means you do not have permissions in the destination project. Check to make sure you have permissions to the project, area path, and iteration path

* I am unable to import work items

  - This usually means you do not have permissions. Check to make sure you have permissions to the project, area path, and iteration path

## **Recommended Documents**

* [Quick guide to default permissions and access for Azure Boards](https://docs.microsoft.com/azure/devops/boards/get-started/permissions-access-boards?view=azure-devops&viewFallbackFrom=azure-devops)
* [About area and iteration (sprint) paths](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops)
* [Azure DevOps Services Status](https://status.dev.azure.com)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
