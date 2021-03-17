<properties
  pagetitle="Customizing Work Item Tracking Issues&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="dahellem,cathmill"
  selfhelptype="Generic"
  supporttopicids="32300884"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopsboardscustomizeworkitemtracking"
  ownershipid="Azure_DevOps_Services" />
# Customizing Work Item Tracking Issues

## **Recommended Steps**

Are you facing one of these common problems?

* Why am I unable to customize a work item?

  - Check to see if you have the correct [process customization permissions](https://docs.microsoft.com/azure/devops/organizations/settings/work/manage-process?view=azure-devops#prerequisites)

  - On-Premises XML model requires Collection Admin permissions and the use of witadmin.exe. Contact your local Collection Administrator for more information. [Learn more](https://docs.microsoft.com/azure/devops/reference/on-premises-xml-process-model?view=azure-devops-2020&viewFallbackFrom=azure-devops).

* Don't see a work item type on the backlog

  - Make sure that the [board level](https://docs.microsoft.com/azure/devops/boards/boards/kanban-overview?view=azure-devops#product-and-portfolio-kanban-boards) matches the work item type you are looking for. For example, the Features board level will show Feature work item types.

  - Check your team board configuration to see if the [backlog navigation level](https://docs.microsoft.com/azure/devops/organizations/settings/select-backlog-navigation-levels?view=azure-devops) is turned on for the work item type you are looking for

  - Check your backlog levels in process configuration to make sure the work item type is associated to the desired level. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/work/customize-process-backlogs-boards?view=azure-devops#add-or-edit-portfolio-backlogs).

* We are not able to run witadmin.exe command on the Azure DevOps Service

  - Witadmin.exe is not supported on the Azure DevOps Service. It is only supported on XML collections on-premises.

* We get errors when trying to copy an inherited process

  - Check to make sure your custom rules are not referencing a field that no longer exists. If so, fix the rule and try again.

* We get errors when cloning a Hosted XML process to Inherited.
  - Not all hosted xml process customizations are supported in Inherited. [Learn more](https://docs.microsoft.com/azure/devops/organizations/settings/work/upgrade-support-hosted-to-inherited?view=azure-devops).

  - Work item type names that have special characters will cause the clone process to fail. You will need to rename your work item types.

## **Recommended Documents**

* [On-premises XML process customization](https://docs.microsoft.com/azure/devops/reference/on-premises-xml-process-model?view=azure-devops-2020&viewFallbackFrom=azure-devops)
* [About process customization and inherited processes](https://docs.microsoft.com/azure/devops/organizations/settings/work/inheritance-process-model?view=azure-devops&tabs=agile-process)
* [Customize your backlogs or boards (Inheritance process)](https://docs.microsoft.com/azure/devops/organizations/settings/work/customize-process-backlogs-boards?view=azure-devops)
* [Add or edit portfolio backlogs](https://docs.microsoft.com/azure/devops/organizations/settings/work/customize-process-backlogs-boards?view=azure-devops#add-or-edit-portfolio-backlogs)
* [Supported operations when moving from Hosted XML to an inherited process](https://docs.microsoft.com/azure/devops/organizations/settings/work/upgrade-support-hosted-to-inherited?view=azure-devops)
* [Copy a process](https://docs.microsoft.com/azure/devops/organizations/settings/work/manage-process?view=azure-devops#copy-a-process)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
