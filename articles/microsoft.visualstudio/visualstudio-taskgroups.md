<properties
  pagetitle="Azure pipelines issues while using Task groups&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742329"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinetaskgroupissues"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while using Task groups

## **Recommended Steps**

Are you facing one of these common problems?

****

* **I want to pass the Resource Group name from the release pipeline to the task group**

    Use the pipeline variable to pass the Resource Group value to the task group.
    

* **I'm unable to add Task Group to a deployment group job**

    In such cases, ensure that it is compatible with an agent, and add a Deployment group to the **runs On** parameter of the job.
    

* **I'm facing an issue with my task group which gives an error, "Missing default value for the variable in Task Group definition."**

    Provide a default value for the variable in the task group definition. [For instructions, see this document](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops#before-you-create-a-task-group).


## **Recommended Documents**

* [Task groups for builds and releases](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops)
* [Create a task group](https://docs.microsoft.com/azure/devops/pipelines/library/task-groups?view=azure-devops#create-a-task-group)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)