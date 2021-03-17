<properties
  pagetitle="Azure Pipelines issues related to triggers"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,vimalt,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742305"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinestriggerissues"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines issues related to triggers

Resolve most issues related to triggers by using the following solutions.

## **Recommended Steps**

The following information applies to customers who have source code in an Azure Repos, GitHub, BitBucket, or Subversion and are having trouble with CI, CD, pull request, or pipeline-to-pipeline triggers. Select the appropriate problem and the repository type below:

Follow through all of these steps before you create a support ticket. If you need to create a ticket, provide information about the path you took and results of the steps you ran in your ticket to expedite the resolution of your problem.

* I am setting up CI (Continuous Integration) or PR (Pull Request) triggers in my YAML pipeline, and they do not work

   -    [Azure Repos Git repo](https://docs.microsoft.com/azure/devops/pipelines/repos/azure-repos-git#failing-triggers)
   -    [GitHub](https://docs.microsoft.com/azure/devops/pipelines/repos/github#failing-triggers)
   -    [GitHub Enterprise](https://docs.microsoft.com/azure/devops/pipelines/repos/github-enterprise#failing-triggers)
   -    [BitBucket Cloud](https://docs.microsoft.com/azure/devops/pipelines/repos/bitbucket#failing-triggers)
   -    [BitBucket server](https://docs.microsoft.com/azure/devops/pipelines/repos/on-premises-bitbucket#failing-triggers)
   -    [TFVC](https://docs.microsoft.com/azure/devops/pipelines/repos/tfvc#ci-triggers)
   -    [Subversion](https://docs.microsoft.com/azure/devops/pipelines/repos/subversion#failing-triggers)	

* I am using scheduled triggers in my YAML pipeline, and the pipeline is not being triggered on schedule

  - Read the suggestions in [scheduled triggers FAQ](https://docs.microsoft.com/azure/devops/pipelines/process/scheduled-triggers#faq).

* I am using pipeline resources in my YAML pipeline, and the pipeline is not being triggered
  - Read the section on [pipeline triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?tabs=yaml) to understand the limitations of this feature.

* I have a classic build or release pipeline, and triggers do not work
  - [Classic release pipeline triggers](https://docs.microsoft.com/azure/devops/pipelines/release/triggers)
  - [Build completion triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?tabs=classic) in classic build pipelines

* My pipeline is triggered, but it is stuck waiting. 
  Go back and change the problem type as follows:

    - Problem type: **Pipelines - Configuring pipelines**
    - Problem subtype: **My pipelines are stuck waiting in a queue**

* My pipeline is triggered, but fails in `checkout` or `get sources` step. 
  Go back and change the problem type as follows:
  
    - Problem type: **Pipelines - Building and testing your application**
    - Problem subtype: **Getting source code from repository into pipeline**

* I have other issues with integrating my pipeline with Azure Repos, GitHub, BitBucket, or Subversion. 
  Go back and change the problem type as follows:
    - Problem type: **Pipelines - Building and testing your application**
    - Problem subtype: **GitHub, BitBucket, SVN integration**

## **Recommended Documents**

* [Triggers for each type of repo](https://docs.microsoft.com/azure/devops/pipelines/build/triggers?view=azure-devops)
* [Scheduled triggers](https://docs.microsoft.com/azure/devops/pipelines/process/scheduled-triggers?view=azure-devops&tabs=yaml)
* [Pipeline completion triggers](https://docs.microsoft.com/azure/devops/pipelines/process/pipeline-triggers?view=azure-devops&tabs=yaml)
* [Classic release management triggers](https://docs.microsoft.com/azure/devops/pipelines/release/triggers?view=azure-devops)
* [YAML syntax for triggers](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema?view=azure-devops&tabs=schema%2Cparameter-schema#triggers)
* [Build Troubleshooting](https://docs.microsoft.com/azure/devops/pipelines/troubleshooting?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)