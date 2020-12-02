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

* Review [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD for CI/CD in Azure Data Factory

* Use custom parameters with [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template) to override default properties during deployment. You can now edit your `arm-template-parameters-definition.Json` directly in ADF UX <br>

* If you reach the Azure Resource Manager template size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits. 

* [Unsupported features](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features):
    * By design, CI/CD publishing **does not allow** for selective publishing subsets of changes. To publish individual changes into production environment, consider using a [hotfix or QFE](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).
    * We do not recommend assigning Azure RBAC controls to individual entities (pipelines, datasets, and so on) in a data factory. For example, if a developer has access to a pipeline or a dataset, they should be able to access all pipelines or datasets in the data factory. If you feel that you need to implement many Azure roles within a data factory, consider deploying a second data factory.
    * You cannot publish from private branches.
    * You cannot host projects on Bitbucket or Gitlab. 

## **Recommended Documents**

1. Continuous integration and delivery of [(CI/CD)](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment) in Azure Data Factory <br>

    * **Be sure to read** [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd)<br>
    * [Hotfix Production Branch Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch) <br>
    * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) <br>
    * [Automate continuous integration Sample and Steps](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases): this example shows how to stop active triggers before deployment and restart them afterwards.

2. Source Control in Azure Data Factory <br>
    
    * **Be sure to read** [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration <br>
    * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch <br>
    * Switch to a different Git repo [Steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo) <br>

3. [Copy or clone a data factory in ADF](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory) <br>

    * [Use Cases](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) <br>
    * [Steps](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) <br>

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
