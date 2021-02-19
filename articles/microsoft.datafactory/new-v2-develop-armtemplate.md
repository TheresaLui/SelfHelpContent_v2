<properties
  pagetitle="Export and import Resource Manager (ARM) templates"
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629439"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="041c38a6103440898124b090511d597a"
  ownershipid="AzureData_DataFactory" />
# Export and import Resource Manager (ARM) templates

Most customers can resolve import/export issues with Azure Resource Manager (ARM) templates using the following steps.

## **Recommended Steps**
  * Use custom parameters with the [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template
) to override default properties during deployment. You can now edit your arm-template-parameters-definition.json directly in ADF UX. <br>
  * The Resource Manager template has several limits. For details, see [Resource Manager Template Limits](https://docs.microsoft.com//azure/azure-resource-manager/templates/error-job-size-exceeded) for details. 
    * Deployment job cannot exceed 1 MB. The job includes metadata about the request. For large templates, the metadata combined with the template can exceed the allowed size for a job.
    * The template can't exceed 4 MB. The 4-MB limit applies to the final state of the template after it has been expanded for resource definitions that use copy to create many instances. The final state also includes the resolved values for variables and parameters.
    * Other limits for the template include 256 parameter, 800 resources etc. 
  * If you reach the Azure Resource Manager template 4MB size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits. 
  * Review [Common errors and messages](https://docs.microsoft.com//azure/data-factory/ci-cd-github-troubleshoot-guide) for troubleshooting CICD, Azure DevOps, and Github issues in ADF. 

## **Recommended Documents**

* Export and import [ARM templates](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#create-a-resource-manager-template-for-each-environment) in data factory <br>
* Copy or clone a [data factory](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory) in ADF
* Integrate the [CI/CD cycle](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment), including the following sections: <br>

  * [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) _(Recommended)_ <br>
  * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) <br>
  * [Automate continuous integration](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases) with Azure Pipelines releases and [deployment template](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-deployment-template) <br>
  * Stop triggers before deployment and [restart them afterwards](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-script-to-stop-and-restart-triggers-and-clean-up) <br>
