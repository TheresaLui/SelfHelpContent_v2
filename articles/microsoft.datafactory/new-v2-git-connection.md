<properties
  pagetitle="Connect to Git Repository"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629453,32629524,32629447"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="fa4bf4772808490c928247f53858e614"
  ownershipid="AzureData_DataFactory" />
# Connect to Git Repository

## **Recommended Steps**

1. You can create an Azure Repos Git repo in a different Azure Active Directory (AD) tenant. To specify a different Azure AD tenant, you need Administrator permissions for the Azure subscription that you're using. 
2. Bitbucket and Gitlab are not currently supported in Azure Data Factory 
3. Git publishing does not allow for selectively publishing a subset of changes. To publish individual changes in a production environment, consider making a hotfix or taking QFE [steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).
4. If you can't publish changes and get the error "This is likely due to publishing outside of Git mode...", this is because your publish branch is out of sync with the master branch. See [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to recover from this state. 
5. When working on a team, there can be instances where you merge changes, but don't want them to be run in elevated environments such as PROD and QA. See [Exposure control and feature flags](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#exposure-control-and-feature-flags) for how to handle this scenario. 
6. GitHub has a known limitation that a maximum of 1,000 entities per resource type (such as pipelines, datasets, triggers) can be fetched from a single GitHub branch. If you reach this limit, split your resources into separate factories. Azure DevOps Git does not have this limitation. 
7. Review [Common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and Github issues in ADF. 

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

  * **Be sure to read** [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD  <br>
  * Hotfix Production Branch [Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch) <br>
  * [Unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features) <br>

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)