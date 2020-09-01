<properties
	pageTitle="Connect to Git Repository"
	description="Connect to Git Repository from ADF Portal"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="fa4bf4772808490c928247f53858e614"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629453, 32629524, 32629447"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Connect to Git Repository

## **Recommended Steps**

1. You can create an Azure Repos Git repo in a different Azure Active Directory tenant. To specify a different Azure AD tenant, you have to have _administrator_ permissions for the Azure subscription that you're using. <br>
2. As of today, Bitbucket is not supported in Azure Data Factory <br>
3. Git publishing does _not_ allow for cherry picking or selective publishing subset of changes. To publish individual changes in production environment, please consider Hot fix or QFE [Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch)

## **Recommended Documents**

* Source Control in Azure Data Factory <br>

  * [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration __please read__ <br>
  * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch <br>
  * Author with [Azure Repos Git integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-azure-repos-git-integration) <br>
  * Author with [GitHub integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-github-integration) <br>
  * Switch to a different Git repo [Steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo) <br>
  * Version control or source control [Documentation](https://docs.microsoft.com//azure/data-factory/source-control#version-control) <br>

* Azure Repos Git

  * Azure Repos Git [Tutorial](https://docs.microsoft.com/azure/devops/repos/git/gitworkflow) by Azure DevOps Services <br>
  * Troubleshooting Guide: [Unable to Connect](https://docs.microsoft.com//azure/devops/reference/error/tf31002-unable-connect-tfs?view=azure-devops)

* Continuous integration and delivery [CI/CD](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment)

  * [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD __please read__ <br>
  * Hot Fix Production Branch [Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch) <br>
  * [Unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features) <br>

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
