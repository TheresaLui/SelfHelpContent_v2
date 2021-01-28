<properties
  pagetitle="Continuous Integration and Delivery with Git Repository Integration"
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629448"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="35b4075ca21d47c7b82383744226a444"
  ownershipid="AzureData_DataFactory" />
# Continuous Integration and Delivery with Git Repository Integration

## **Recommended Steps**

 

* Use custom parameters with the [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template) to override default properties during deployment. You can now edit your `arm-template-parameters-definition.Json` directly in ADF UX. 

* If you reach the Azure Resource Manager template size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits

* When working on a team, if you need to merge changes, but don't want them to be run in elevated environments such as PROD and QA, see [Exposure control and feature flags](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#exposure-control-and-feature-flags) 

* [Unsupported features](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features):
    * By design, CI/CD publishing does not allow selectively publishing subsets of changes. To publish individual changes into production environment, consider using a [hotfix or QFE](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).
    * We do not recommend assigning Azure RBAC controls to individual entities (pipelines, datasets, and so on) in a data factory. For example, if a developer has access to a pipeline or a dataset, they should be able to access all pipelines or datasets in the data factory. If you feel that you need to implement many Azure roles within a data factory, consider deploying a second data factory.
    * You cannot publish from private branches.
    * You cannot host projects on Bitbucket or Gitlab. 
    
* If you're experiencing issues, refer to this article to [troubleshoot CI-CD, Azure DevOps, and Github issues in ADF](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide).

## **Recommended Documents**

1. Continuous integration and delivery of [(CI/CD)](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment) in Azure Data Factory 
    * **Be sure to read** [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd)
    * [Hotfix Production Branch Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch) 
    * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) 
    * [Automate continuous integration Sample and Steps](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases): this example shows how to stop active triggers before deployment and restart them afterwards.

2. Source Control in Azure Data Factory 
    
    * **Be sure to read** [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration 
    * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch
    * Switch to a different Git repo [Steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo) 

3. [Copy or clone a data factory in ADF](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory)

    * [Use Cases](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) 
    * [Steps](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) 

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
