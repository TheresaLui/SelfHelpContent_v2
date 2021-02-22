<properties
  pagetitle="Azure Pipelines licensing and parallel jobs issues"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742317"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelineslicensing"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines licensing and parallel jobs issues

Most users can resolve issues concerning Azure Pipelines licensing and parallel jobs by using the following information.

## **Recommended Steps**

* I need to **buy more concurrency** or parallel jobs<br>
  - Follow the [instructions to purchase additional parallel jobs for private projects](https://docs.microsoft.com/azure/devops/organizations/billing/buy-more-build-vs?view=azure-devops) 
  - If you maintain an open-source project, then continue and create a new support ticket to get additional concurrency

* I wanted to run two jobs in parallel. I purchased an extra Microsoft-hosted parallel job on top of my free limit. However, I can still run only one job at a time.<br>
  - Your first purchase removes the limits on your free allocation. It increases the number of minutes to unlimited and the maximum time for each job to 6 hours. It doesn't give you a second parallel job in addition to your free limit.
  - To be able to run two jobs in parallel, you need to buy two parallel jobs. See [Paying for parallel jobs](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops).

* I purchased additional parallel jobs but my jobs still time out after 60 minutes<br>
  - By purchasing Microsoft-hosted parallel jobs, you can increase your timeouts up to 6 hours per job. The default timeout is still 60 minutes.
  - To increase the timeout in YAML pipelines, specify the [timeoutInMinutes](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=yaml#timeouts) property in the YAML file.
  - To increase the timeout in classic pipelines, specify the value of timeout in the [**Options** tab](https://docs.microsoft.com/azure/devops/pipelines/process/phases?view=azure-devops&tabs=classic#timeouts).

* My pipelines are stuck waiting in a queue although I have a number of parallel jobs

  - Go back and change the problem type as follows:<br>
    Problem type: **Pipelines - Configuring pipelines**<br>
    Problem subtype: **My pipelines are stuck waiting in a queue**

* I purchased additional parallel job but still have a problem with Microsoft-hosted agents

  - Go back and change the problem type as follows:<br>
    Problem type: **Pipelines - Configuring pipelines**<br>
    Problem subtype: **Microsoft-hosted agents - disk space, IP address range, etc**

## **Recommended Documents**

* [Parallel jobs](https://docs.microsoft.com/azure/devops/pipelines/licensing/concurrent-jobs?view=azure-devops)
* [Microsoft-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/hosted?view=azure-devops)
* [Self-hosted agents](https://docs.microsoft.com/azure/devops/pipelines/agents/agents?view=azure-devops#install)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
