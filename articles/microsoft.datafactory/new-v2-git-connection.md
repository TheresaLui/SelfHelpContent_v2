<properties
  pagetitle="Connect to Git Repository"
  service="microsoft.datafactory"
  resource="factories"
  ms.author="chez,haoc,nimoolen"
  selfhelptype="Generic"
  supporttopicids="32629453,32629524,32629447"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="fa4bf4772808490c928247f53858e614"
  ownershipid="AzureData_DataFactory" />
# Connect to Git Repository

Most customers can resolve connection issues to the Git repository using the following guidance.

In this article:
1. [Before you begin...](#**before-you-begin...**)
1. [Known limitations](#**known-limitations**)
1. [Connecting to GitHub for the first time](#**connecting-to-github-for-the-first-time**)
1. [Using an Azure DevOps repo in another tenant](#**using-an-azure-devops-repo-in-another-tenant**)
1. [Selective publishing](#**selective-publishing**)
1. [Error: "This is likely due to publishing outside of Git mode..."](#**error:-"this-is-likely-due-to-publishing-outside-of-git-mode..."**)
1. [Running only in test env.](#**running-only-in-test-env.**)
1. [Other common errors](#**other-common-errors**)
1. [Recommended Documents](#**recommended-documents**)

## **Recommended Steps**

### **Before you begin...**
Ensure all of the following is true:
- You have admin permissions on the Git repo
- You have write access at the factory level of your ADF resource
- If using Azure DevOps, either the Data Factory and repo are in the same tenant *or* you have administrator permissions at the Azure subscription level
- If using Azure DevOps, the same email/AAD account is used for both ADF and your Git repo

### **Known limitations**
- Bitbucket and GitLab are not currently supported in Azure Data Factory (ADF)
- GitHub allows a maximum of 1,000 entities per resource type (such as pipelines, datasets, triggers) in a single branch. If you reach this limit, split your resources into separate factories. Azure DevOps does not have this limitation.

### **Connecting to GitHub for the first time**

When [connecting to Github for the first time in Azure Data Factory](https://docs.microsoft.com//azure/data-factory/source-control#connecting-to-github-for-the-first-time-in-azure-data-factory), make sure permission is granted for ADF to access the organization. You may need to ask an admin to manually grant the permission through Github.

### **Using an Azure DevOps repo in another tenant**

You can select an Azure DevOps Git repository in a different Azure Active Directory (AD) tenant during the Git configuration in the ADF UI. To specify a different Azure AD tenant, you need Administrator permissions for the Azure subscription that you're using. 


### **Selective publishing**

Git publishing does not allow publishing for a subset of changes. To publish individual changes in a production environment, consider making a hotfix or taking [QFE steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).

### **Error: "This is likely due to publishing outside of Git mode..."**
If you can't publish changes and receive the error "This is likely due to publishing outside of Git mode...", your publish branch is out of sync with the master branch. To resolve this issue, see [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration). 

### **Running only in test env.**
When working on a team, there can be instances where you merge changes, but don't want them to be run in elevated environments such as PROD and QA. See [Exposure control and feature flags](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#exposure-control-and-feature-flags) for how to handle this scenario. 

### **Other common errors**
Review [common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and GitHub issues in ADF. 

## **Recommended Documents**

- Learn about [Azure DevOps permissions and access](https://docs.microsoft.com//azure/devops/organizations/security/permissions-access?view=azure-devops)  




- Source Control in Azure Data Factory
  - **Strongly recommended:** [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration
  - [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch
  - Author with [Azure Repos Git integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-azure-repos-git-integration)
  - Author with [GitHub integration](https://docs.microsoft.com//azure/data-factory/source-control#author-with-github-integration)
  - Switch to a different Git repo [steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo)
  - Version control or source control [documentation](https://docs.microsoft.com//azure/data-factory/source-control#version-control)  




- Azure Repos Git
  - Azure Repos Git [tutorial](https://docs.microsoft.com/azure/devops/repos/git/gitworkflow) by Azure DevOps Services
  - Troubleshooting Guide: [Unable to Connect](https://docs.microsoft.com//azure/devops/reference/error/tf31002-unable-connect-tfs?view=azure-devops)  




- Continuous integration and delivery [CI/CD](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment)
  - **Strongly recommended:** [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD
  - Hotfix Production Branch [Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch)
  - [Unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features)  
 



- Azure Data Factory FAQ & Feature Requests
  - [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
  - [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
  - [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
