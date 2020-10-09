<properties
    pageTitle="Azure Boards Work Item Performance"
    description="Issues with work item performance"
    infoBubbleText="Azure Boards work item performance"
    service="microsoft.visualstudio"
    resource="account"
    authors="danhellem"
    ms.author="dahellem"
    articleId="AZDevOpsBoardsWorkItemPerformance"
    supportTopicIds="32260215"
    diagnosticScenario=""
    selfHelpType="generic"
    resourceTags=""
    productPesIds="15543"
    cloudEnvironments="public, fairfax, usnat, ussec"
    ownershipId="Azure_DevOps_Services"
/>

# Work Item Performance Issues

## **Recommended Steps**

Are you facing one of these common problems?

* Loading a work item is slow. How do we improve performance?

  - Adding lots of custom fields, rules, and extensions can slow down form performance. Try one or more of the following:
    - Remove fields that are not used or can be combined into another field
    - Remove extensions that are not needed
    - Try grouping non-critical fields and placing them on a separate page (tab)

* My Boards and Backlogs are reaching the [work item limits](https://docs.microsoft.com/azure/devops/organizations/settings/work/object-limits?view=azure-devops). Is there a way to increase the limits?

  - Unfortunately the limits cannot be increased. These are in place to ensure the product performance at acceptable levels
  - Use teams and area paths to break up the work to more manageable levels. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops)
  - See if it makes sense to split the work into more than one project
  - Delete work items that are not longer needed or used

## **Recommended Documents**

* [About process customization and inherited processes](https://docs.microsoft.com/azure/devops/organizations/settings/work/inheritance-process-model?view=azure-devops&tabs=agile-process)
* [Work tracking, process, and project limits](https://docs.microsoft.com/azure/devops/organizations/settings/work/object-limits?view=azure-devops)
* [Azure DevOps Services Status](https://status.dev.azure.com)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
