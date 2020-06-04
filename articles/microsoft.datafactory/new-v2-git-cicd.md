<properties
	pageTitle="Continuous Integration and Delivery in ADF"
	description="CI/CD with Azure Data Factory"
	infoBubbleText=""
	authors="chez-charlie"
	ms.author="chez"
	articleId="35b4075ca21d47c7b82383744226a444"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32629448"
	resourceTags=""
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureData_DataFactory"
/>

# Continuous Integration and Delivery with Git Repository Integration

## **Recommended Steps**

* Please consider the [Best practices](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) for CI/CD for CI/CD in Azure Data Factory
* Please be aware of the [unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features)
* By design, CI/CD publishing does _not_ allow for cherry picking and/or selective publishing subset of changes. To publish individual changes into production environment, please consider [Hot fix or QFE](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch)

## **Recommended Documents**

1. Continuous integration and delivery [(CI/CD)](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment) in Azure Data Factory <br>

    * [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) __(please read)__ <br>
    * [Hot Fix Production Branch Steps](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#hot-fix-production-branch) <br>
    * [Unsupported features list](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#unsupported-features) <br>
    * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) <br>
    * [Automate continuous integration Sample and Steps](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases): this example shows how to stop active triggers before deployment and restart them afterwards
    * Use custom parameters with [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template
) to override default properties during deployment<br>
    * [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates): this is the workaround for Azure Resource Manager template size limits

2. Source Control in Azure Data Factory <br>
    
    * [Best practices](https://docs.microsoft.com//azure/data-factory/source-control#best-practices-for-git-integration) for Git Integration __(please read)__<br>
    * [Troubleshooting Git integration](https://docs.microsoft.com//azure/data-factory/source-control#troubleshooting-git-integration) to deal with stale publish branch <br>
    * Switch to a different Git repo [Steps](https://docs.microsoft.com//azure/data-factory/source-control#switch-to-a-different-git-repo) <br>

3. Copy or clone a data factory in ADF: [Document](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory) <br>

    * [Use Cases](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) <br>
    * [Steps](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory#use-cases-for-cloning-a-data-factory) <br>

**Azure Data Factory Feature Requests**

- [Azure Data Factory V1 FAQ](https://docs.microsoft.com/azure/data-factory/v1/data-factory-faq)
- [Azure Data Factory V2 FAQ](https://docs.microsoft.com//azure/data-factory/frequently-asked-questions)
- [Feature Request](https://feedback.azure.com/forums/270578-azure-data-factory)
