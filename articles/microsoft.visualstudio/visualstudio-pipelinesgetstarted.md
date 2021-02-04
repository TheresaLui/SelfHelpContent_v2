<properties
	pageTitle="Azure Pipelines Getting Started"
	description="Azure Pipelines help getting started"
	infoBubbleText="Azure Pipelines help getting started"
	service="microsoft.visualstudio"
	resource="account"
	authors="vijayma,v-abiss"
	ms.author="vijayma,v-abiss"
	articleId="AZDevOpsPipelinesGetStarted"
	supportTopicIds="32742316"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure Pipelines Getting Started

## **Recommended Steps**

In general, our support team is equipped to handle specific issues that arise when you use Azure Pipelines. However, they are not equipped to provide broad process guidance or training. So, we encourage you to first read the [documentation](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops), experiment on your own, and then come back with a more specific question. Use the search feature in the documentation to get help more easily. Here are some pointers to help you get started:

* I am new to Pipelines. How do I get started?

  Look at our documentation. Here are the best places to get started:
  - [Create your first pipeline](https://docs.microsoft.com/azure/devops/pipelines/create-first-pipeline?view=azure-devops)
  - [Customize your pipeline](https://docs.microsoft.com/azure/devops/pipelines/customize-pipeline?view=azure-devops)
  - [User experience](https://docs.microsoft.com/azure/devops/pipelines/get-started/multi-stage-pipelines-experience?view=azure-devops)

  After you have the basics, you can dive into more concepts. Look at the **Pipelines basics** folder in our [documentation](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops)

* I am confused about build vs. release pipelines, classic vs. YAML pipelines. 

  Azure Pipelines has evolved through several iterations while retaining legacy models for backward compatibility. If you started creating pipelines today, you should only look at YAML pipelines and not classic pipelines. For more discussion on this topic, see [CI, CD, YAML and Classic](https://docs.microsoft.com/azure/devops/pipelines/get-started/pipelines-get-started?view=azure-devops)

* I am not sure how I should set up pipelines to deploy test and production environments with the Git branching model that I have.

  You can follow a release branch model, where you create a release branch for each deployment. You can follow a trunk model where every change to a main branch is pushed all the way to production. There are also several other branching models possible. We don't provide specific guidance on how to create pipelines in each of these cases, because the requirements and constraints for each case are often different. Here are some documents that provide some examples, which you can draw from:

  - [Build multiple branches](https://docs.microsoft.com/azure/devops/pipelines/build/ci-build-git?view=azure-devops&tabs=yaml)
  - [Deploy classic releases from multiple branches](https://docs.microsoft.com/azure/devops/pipelines/release/deploy-multiple-branches?view=azure-devops)

* I am new to YAML pipelines, and I am not sure how I should secure my production environments.

  Read our [guidance](https://docs.microsoft.com/azure/devops/pipelines/security/overview?view=azure-devops) on how to secure YAML pipelines.

* How can I set up my release pipeline in YAML?

  In YAML pipelines, we recommend that you put your deployment steps in a special type of job called a **deployment job**. Read our guidance and define the release pipeline for your project by using of the YAML schema outlined for [Deployment Jobs](https://docs.microsoft.com/azure/devops/pipelines/process/deployment-jobs?view=azure-devops).

## **Recommended Documents**

* [Azure Pipelines Docs](https://docs.microsoft.com/azure/devops/pipelines/?view=azure-devops)
* [YAML schema](https://docs.microsoft.com/azure/devops/pipelines/yaml-schema?view=azure-devops)
* [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
* [Azure DevOps Services Status](https://status.dev.azure.com)
* [Deployment Jobs](https://docs.microsoft.com/azure/devops/pipelines/process/deployment-jobs?view=azure-devops)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)

