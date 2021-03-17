<properties
  pagetitle="Kanban and Sprint Board Issues&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="dahellem,cathmill"
  selfhelptype="Generic"
  supporttopicids="32260185"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopsboardskanbanandsprintboard"
  ownershipid="Azure_DevOps_Services" />
# Kanban and Sprint Board Issues

## **Recommended Steps**

Are you facing one of these common problems?

**Why can't I find an item on the kanban board?**

  - Check and make sure your filter is showing all work items. If you are filtering by work item type, state, etc., you may be hiding some work items from being displayed. [Learn more](https://docs.microsoft.com/azure/devops/boards/boards/filter-kanban-board?view=azure-devops).

  - If you have a large backlog, your work item may be on the board but it appears lost in a sea of work items. Try clearing the filter entirely and then enter the title name or a few [keywords in a new filter](https://docs.microsoft.com/azure/devops/boards/boards/filter-kanban-board?view=azure-devops#filter-using-select-field-values). This will narrow down the list of work cards that match those words.

  - The number of new and closed work items is limited to 20 at time. Try using the **show more items** link at the bottom of the column to load more items.

  - Work items on a board must set to an area path and iteration path associated to that team, or those items will not be displayed. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops).

  - Make sure that the [board level](https://docs.microsoft.com/azure/devops/boards/boards/kanban-overview?view=azure-devops#product-and-portfolio-kanban-boards) matches the work item type you are looking for. For example, the Features board level will show Feature work item types.

  - Check your team board configuration to see if the [backlog navigation level](https://docs.microsoft.com/azure/devops/organizations/settings/select-backlog-navigation-levels?view=azure-devops) is turned on for the work item type you are looking for

  - If you are missing Bugs on your board, make sure you are [showing bugs on the backlogs and boards](https://docs.microsoft.com/azure/devops/organizations/settings/show-bugs-on-backlog?toc=%2Fazure%2Fdevops%2Fboards%2Ftoc.json&bc=%2Fazure%2Fdevops%2Fboards%2Fbreadcrumb%2Ftoc.json&view=azure-devops)

  - Check the recycle bin to see of the work item was deleted. [Learn more](https://docs.microsoft.com/azure/devops/boards/backlogs/remove-delete-work-items?view=azure-devops).

**Why don't I see all the work items on the kanban board?**

  - The number of items on your board exceeds the configured limit of 1,000. [Learn more](https://docs.microsoft.com/azure/devops/user-guide/service-limits?view=azure-devops).

  - The new and completed columns are limited to 20 items at a time. This is done to improve performance allowing teams to focus on the active work. You can use the **show more items** link to fetch more work items in those columns.

## **Recommended Documents**

* [Filter your Kanban board](https://docs.microsoft.com/azure/devops/boards/boards/filter-kanban-board?view=azure-devops)
* [Product and portfolio Kanban boards](https://docs.microsoft.com/azure/devops/boards/boards/kanban-overview?view=azure-devops#product-and-portfolio-kanban-boards)
* [Select backlog navigation levels for your team](https://docs.microsoft.com/azure/devops/organizations/settings/select-backlog-navigation-levels?view=azure-devops)
* [About area and iteration (sprint) paths](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops)
* [Show bugs on backlogs and boards](https://docs.microsoft.com/azure/devops/organizations/settings/show-bugs-on-backlog?toc=%2Fazure%2Fdevops%2Fboards%2Ftoc.json&bc=%2Fazure%2Fdevops%2Fboards%2Fbreadcrumb%2Ftoc.json&view=azure-devops)
* [Remove or delete work items](https://docs.microsoft.com/azure/devops/boards/backlogs/remove-delete-work-items?view=azure-devops)
* [Work tracking, process, and project limits](https://docs.microsoft.com/azure/devops/organizations/settings/work/object-limits?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
