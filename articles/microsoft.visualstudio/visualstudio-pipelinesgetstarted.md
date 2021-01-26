<properties
  pagetitle="Azure Pipelines Getting Started&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="vijayma,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742316"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelinesgetstarted"
  ownershipid="Azure_DevOps_Services" />
# Azure Pipelines Getting Started

## **Recommended Steps**

In general, our support team is equipped to handle specific issues that arise when you use Azure Pipelines. They are not equipped to provide broad process guidance or training. So, we encourage you to first read the [docs](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops), experiment, and then come back with a more specific question. Use the search feature in docs to get help more easily. Here are some pointers to help you get started.

* I am new to Pipelines. How do I get started?

  Look at our docs. Here are the best places to get started:
  - [Create your first pipeline](https://docs.microsoft.com/azure/devops/pipelines/create-first-pipeline?view=azure-devops)
  - [Customize your pipeline](https://docs.microsoft.com/azure/devops/pipelines/customize-pipeline?view=azure-devops)
  - [User experience](https://docs.microsoft.com/azure/devops/pipelines/get-started/multi-stage-pipelines-experience?view=azure-devops)

  Once you have the basics, you can dive into more concepts. Look at the **Pipelines basics** folder in our [docs](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops)

* Confused about build vs release pipelines, classic vs YAML pipelines? 

  Azure Pipelines has evolved through several iterations while retaining legacy models for backward compatibility. If you were to start creating pipelines today, you should only look at YAML pipelines and not classic. For more discussion on this topic, see [CI, CD, YAML and Classic](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops)

* I am not sure how I should set up pipelines to deploy test and production environments with the Git branching model that I have

  You may follow a release branch model, where you create a release branch for each deployment. You may follow a trunk model where every change to a main branch is pushed all the way to production. And, there are several other branching models possible. We do not provide specific guidance for how to create pipelines in each of these cases as the requirements and constraints for each case are often different. Here are some documents that provide some examples, which you can draw from:

  - [Build multiple branches](https://docs.microsoft.com/azure/devops/pipelines/build/ci-build-git?view=azure-devops&tabs=yaml)
  - [Deploy classic releases from multiple branches](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-multiple-branches?view=azure-devops)

* I am new to YAML pipelines, and I am not sure how I should secure my production environments

  Read our [guidance](https://docs.microsoft.com/azure/devops/pipelines/security/overview?view=azure-devops) on how to secure YAML pipelines.

## **Recommended Documents**

* [Azure Pipelines Docs](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops)
* [YAML schema](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)