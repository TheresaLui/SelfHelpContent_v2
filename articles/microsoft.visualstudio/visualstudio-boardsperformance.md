<properties
  pagetitle="Work Item Performance Issues&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="dahellem,cathmill"
  selfhelptype="Generic"
  supporttopicids="32260215"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopsboardsworkitemperformance"
  ownershipid="Azure_DevOps_Services" />
# Work Item Performance Issues

Resolve common issues around work item performance with the following solutions.

## **Recommended Steps**

**Loading a work item is slow. How do we improve performance?**

  - Adding lots of custom fields, rules, and extensions can slow down form performance. Try one or more of the following:
    - Remove fields that are not used or can be combined into another field
    - Remove extensions that are not needed
    - Try grouping non-critical fields and placing them on a separate page (tab)

**My Boards and Backlogs are reaching the [work item limits](https://docs.microsoft.com/azure/devops/organizations/settings/work/object-limits?view=azure-devops). Is there a way to increase the limits?**

  - Unfortunately the limits cannot be increased. The established limits ensure the product performance at acceptable levels.
  - Use teams and area paths to break up the work to more manageable levels. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/about-areas-iterations?view=azure-devops).
  - Determine whether it makes sense to split the work into more than one project
  - Delete work items no longer needed or used

## **Recommended Documents**

* [About process customization and inherited processes](https://docs.microsoft.com/azure/devops/organizations/settings/work/inheritance-process-model?view=azure-devops&tabs=agile-process)
* [Work tracking, process, and project limits](https://docs.microsoft.com/azure/devops/organizations/settings/work/object-limits?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
