<properties
  pagetitle="Work Item Permission Issues&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="dahellem,cathmill"
  selfhelptype="Generic"
  supporttopicids="32453004"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopsboardspermissions"
  ownershipid="Azure_DevOps_Services" />
# Work Item Permission Issues

Resolve common issues with work item permissions by using these recommendations.

## **Recommended Steps**

* **I am unable to access a board or backlogs**

   Check to make sure you have [permissions to the team backlog or board](https://docs.microsoft.com/azure/devops/boards/get-started/permissions-access-boards?view=azure-devops).

* **I am unable to save a work item**

  Check to make sure you have [permissions to the project, area path, and iteration path where you are saving the work item](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops).

* **I can't assign a work item to a specific person**

   If you attempt to assign a work item to a person who has never logged into the project, you may get an error. The resolve this, have the person log into the project. This will sync the AAD identity into Azure DevOps.

* **I am not able to move a work item from one project to another**

   This usually means you do not have permissions in the destination project. Check to make sure you have permissions to the project, area path, and iteration path.

* **I am unable to import work items**

   This usually means you do not have permissions. Check to make sure you have permissions to the project, area path, and iteration path.

## **Recommended Documents**

* [Quick guide to default permissions and access for Azure Boards](https://docs.microsoft.com/azure/devops/boards/get-started/permissions-access-boards?view=azure-devops&viewFallbackFrom=azure-devops)
* [About area and iteration (sprint) paths](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
