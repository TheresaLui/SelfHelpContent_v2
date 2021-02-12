<properties
  pagetitle="Export and import Resource Manager (ARM) templates&#xD;"
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629439"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="041c38a6103440898124b090511d597a"
  ownershipid="AzureData_DataFactory" />
# Export and import Resource Manager (ARM) templates

## **Recommended Steps**
  * Use custom parameters with the [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template
) to override default properties during deployment. You can now edit your arm-template-parameters-definition.json directly in ADF UX. <br>
  * If you reach the Azure Resource Manager template size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits. 
  * Review [Common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and Github issues in ADF. 

## **Recommended Documents**

* Export and import [ARM templates](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#create-a-resource-manager-template-for-each-environment) in data factory <br>
* Copy or clone a [data factory](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory) in ADF
* Integrate the [CI/CD cycle](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment), including the following sections: <br>

  * [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) _(Recommended)_ <br>
  * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) <br>
  * [Automate continuous integration](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases) with Azure Pipelines releases and [deployment template](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-deployment-template) <br>
  * Stop triggers before deployment and [restart them afterwards](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-script-to-stop-and-restart-triggers-and-clean-up) <br>