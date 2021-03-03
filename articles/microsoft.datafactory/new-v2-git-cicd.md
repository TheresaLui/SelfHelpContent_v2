<properties
  pagetitle="Continuous Integration and Delivery with Git Repository Integration"
  ms.author="nimoolen,fangl"
  selfhelptype="Generic"
  supporttopicids="32629448"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="35b4075ca21d47c7b82383744226a444"
  ownershipid="AzureData_DataFactory" />
# Continuous Integration and Delivery with Git Repository Integration

## **Recommended Steps**


 ### **Known limitations**

See all [unsupported features](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features):

- Bitbucket and GitLab are not currently supported in Azure Data Factory (ADF)
- We do not recommend assigning Azure RBAC controls to individual entities (pipelines, datasets, and so on) in a data factory. For example, if a developer has access to a pipeline or a dataset, they should be able to access all pipelines or datasets in the data factory. If you feel that you need to implement many Azure roles within a data factory, consider deploying a second data factory.
- You cannot publish from private branches

### **Best Practice**
[Best practices](https://docs.microsoft.com/azure/data-factory/)

### **Custom parameters**

Use custom parameters with the [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template) to override default properties during deployment. You can now edit your `arm-template-parameters-definition.Json` directly in ADF UX. 

### **Selective publishing**

Git publishing does not allow publishing for a subset of changes. To publish individual changes in a production environment, consider making a hotfix or taking [QFE steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch).

### **Azure Resource Manager template size limit**

If you reach the Azure Resource Manager template size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits.

### **Running only in test env.**
When working on a team, there can be instances where you merge changes, but don't want them to be run in elevated environments such as PROD and QA. See [Exposure control and feature flags](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#exposure-control-and-feature-flags) for how to handle this scenario. 

### **Other common errors**
Review [common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and GitHub issues in ADF. 


## **Recommended Documents**

* Continuous integration and delivery of [(CI/CD)](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment) in Azure Data Factory 
    * **Strongly recommended:** [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd)  
    
    * [Hotfix Production Branch Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch)   
    * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle)  
    * [Automate continuous integration Sample and Steps](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases): this example shows how to stop active triggers before deployment and restart them afterwards.

* Source Control in Azure Data Factory 
    
    * **Strongly recommended:** [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration 
    * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch
    * Switch to a different Git repo [Steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo)
    
* [Copy or clone a data factory in ADF](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory)

    * [Use Cases](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) 
    * [Steps](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) 

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
