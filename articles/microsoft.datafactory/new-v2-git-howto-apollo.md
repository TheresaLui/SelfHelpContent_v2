<properties
  pagetitle="Git Repository and Version Control - How To"
  description="Apollo migrated file - Git How To"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="susabat"
  selfhelptype="Apollo"
  productpesids="15613"
  cloudenvironments="fairfax,mooncake,public,usnat,ussec,blackforest"
  disableclouds=""
  articleid="new-v2-git-howto-apollo"
  ownershipid="AzureData_DataFactory"
  supportTopicIds="7cd57f4d-3bc4-3df2-15ee-3a669d979219"
  resourceRequired="false"
/>

# Git Repository and Version Control - How To

## Git Repository and Version Control - How To

Continuous integration is the practice of testing each change made to your codebase automatically. Continuous delivery follows the testing that happens during continuous integration and pushes changes to a staging or production system.

In Azure Data Factory, continuous integration and delivery (CI/CD) means moving Data Factory pipelines from one environment (development, test, production) to another.
Azure Data Factory utilizes Azure Resource Manager templates to store the configuration of your various ADF entities (pipelines, datasets, data flows, and so on). 

There are two suggested methods to promote a data factory to another environment. Most users can resolve issues related to Git Repo in the Git repository by following the guidance below.

<br>

### Recommended steps

1. If you are trying to connect from Azure Data Factory, verify the following: credentials match for both Azure DevOps and Azure Data Factory, Azure DevOps and Azure Data Factory are in the same tenant, and the user has sufficient permissions on the Git account.  

2. You can create an Azure Repos Git repository in a different Azure Active Directory (AD) tenant. To specify a different Azure AD tenant, you need Administrator permissions for the Azure subscription that you are using. 

3. Bitbucket and GitLab are not currently supported in Azure Data Factory.

4. When [connecting to Github for the first time in Azure Data Factory](https://docs.microsoft.com//azure/data-factory/source-control#connecting-to-github-for-the-first-time-in-azure-data-factory), make sure permission is granted for ADF to access the organization. You may need to ask an admin to manually grant the permission through Github. 

5. Git publishing does not allow publishing for a subset of changes. To publish individual changes in a production environment, consider making a hotfix or taking [QFE steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).

6. If you can't publish changes and receive the error *This is likely due to publishing outside of Git mode...*, your publish branch is out of sync with the master branch. To resolve this issue, see [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration). 

7. When working on a team, there can be instances where you merge changes, but don't want them to be run in elevated environments such as PROD and QA. See [Exposure control and feature flags](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#exposure-control-and-feature-flags) for how to handle this scenario. 

8. GitHub has a known limitation that a maximum of 1,000 entities per resource type (such as pipelines, datasets, triggers) can be fetched from a single GitHub branch. If you reach this limit, split your resources into separate factories. Azure DevOps Git does not have this limitation. 

9. Review [Common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and GitHub issues in ADF. 

10. Improvements have been made in publishing ADF templates automatically without clicking a button in ADF portal. The NPM module installation automates ADF publishing and enables the **true** CI/CD process. Please follow [ADF CI/CD Improvements](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment-improvements)

<br>

### Recommended documents

* Default permissions and access for [Azure DevOps](https://docs.microsoft.com//azure/devops/organizations/security/permissions-access?view=azure-devops)
  
* Source Control in Azure Data Factory

  * **Strongly recommended:** [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration
  * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch
  * Author with [Azure Repos Git integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-azure-repos-git-integration)
  * Author with [GitHub integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-github-integration)
  * Switch to a different Git repo [steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo)
  * Version control or source control [documentation](https://docs.microsoft.com//azure/data-factory/source-control#version-control)

* Azure Repos Git

  * Azure Repos Git [tutorial](https://docs.microsoft.com/azure/devops/repos/git/gitworkflow) by Azure DevOps Services
  * Troubleshooting Guide: [Unable to Connect](https://docs.microsoft.com//azure/devops/reference/error/tf31002-unable-connect-tfs?view=azure-devops)

* Continuous integration and delivery [CI/CD](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment)

  * **Strongly recommended:** [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD
  * Hotfix Production Branch [Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch)
  * [Unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features)
 

**Azure Data Factory FAQs and Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)

<br>

### More resources

Here are additional relevant articles based on the __summary__ you provided
<azureKB>
    <client>Portal</client>
</azureKB>
