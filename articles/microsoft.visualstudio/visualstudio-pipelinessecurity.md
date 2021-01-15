<properties
  pagetitle="Azure Pipelines Security and Permissions Issues&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742332"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinessecurityissues"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines Security and Permissions Issues

Resolve common issues with Azure Pipelines security and permissions with the following resources.

## **Recommended Steps**


* I can't check out a repository from another project, or I get an error during the check-out step: "remote: TF401019: The Git repository with name or identifier XYZ does not exist or you do not have permissions for the operation you are attempting" 

  This is usually caused by the [job access token](https://docs.microsoft.com/azure/devops/pipelines/process/access-tokens?view=azure-devops&tabs=yaml) not having access to the repository. See [Failing checkout](https://docs.microsoft.com/azure/devops/pipelines/repos/azure-repos-git?view=azure-devops&tabs=yaml#failing-checkout) in our docs for ways of fixing this problem.

* For my YAML pipelines, why am I prompted to **authorize resources** the first time I try to check out a different repository?

  See this [FAQ](https://docs.microsoft.com/azure/devops/pipelines/repos/multi-repo-checkout?view=azure-devops#why-am-i-am-prompted-to-authorize-resources-the-first-time-i-try-to-check-out-a-different-repository) in multi-repository checkout.

* How do I control the permissions on stages in **YAML pipelines**?

  Since YAML pipelines are represented through YAML files in your repository, the protection on stages or environments is done differently (from classic release pipelines).
  - First, read about [protecting resources in YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/security/resources?view=azure-devops)
  - Then, understand [security through templates in YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/security/templates?view=azure-devops)
  - Finally, review [security best practices for YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/security/overview?view=azure-devops)

* I get an error when **accessing a package feed** from a different project.

  The [job access token](https://docs.microsoft.com/azure/devops/pipelines/process/access-tokens?view=azure-devops&tabs=yaml) may not have access to the feed. You can fix this in one of the following two ways:
  - Changing the [job authorization scope](https://docs.microsoft.com/azure/devops/pipelines/process/access-tokens?view=azure-devops&tabs=yaml#job-authorization-scope) to be the entire project collection.
  - Explicitly granting access for the [build service account](https://docs.microsoft.com/azure/devops/pipelines/process/access-tokens?view=azure-devops&tabs=yaml#build-service-account) to the feed.

* I do not see a particular **button or a menu item** in the UI.

  You do not have permissions to perform that action. To understand what permissions you must be granted, see:
  - [Pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#pipeline-permissions) for classic build and YAML pipelines
  - [Release permissions](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#release-permissions) for classic release pipelines
  - [Library roles and permissions](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#library-roles-and-permissions) for permissions on service connections, variable groups, and secure files
  - [Agent pool permissions](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser#security) for permissions on agent pools
  - [Environment permissions](https://docs.microsoft.com/azure/devops/pipelines/process/environments?view=azure-devops#security) for permissions on environments
  - [Deployment group permissions](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops#deployment-pool-security-roles) for permissions on deployment groups

* I am unable to **add agents** to a pool although I am an administrator on the pool.

  There are two places where agent pools are managed in the UI. In the **Organization** settings, you manage who can add agents to the pool. In the **Project** settings, you manage who can use the pool in that project. You may be looking at the project settings instead of organization settings. For more information about these two levels, see [Agent pool security](https://docs.microsoft.com/azure/devops/pipelines/agents/pools-queues?view=azure-devops&tabs=yaml%2Cbrowser#security).

## **Recommended Documents**

* [Pipeline permissions](https://docs.microsoft.com/azure/devops/pipelines/policies/permissions?view=azure-devops)
* [Multi-repository checkout in YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/repos/multi-repo-checkout?view=azure-devops)
* [Protecting resources in YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/security/resources?view=azure-devops)
* [Security through templates in YAML pipelines](https://docs.microsoft.com/azure/devops/pipelines/security/templates?view=azure-devops)
* [Security best practices](https://docs.microsoft.com/azure/devops/pipelines/security/overview?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
