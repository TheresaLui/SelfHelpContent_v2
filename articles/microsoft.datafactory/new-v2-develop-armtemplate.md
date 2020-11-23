<properties
  pagetitle="Export and Import Resource Manager (ARM) Templates&#xD;"
  ms.author="chez,haoc"
  selfhelptype="Generic"
  supporttopicids="32629439"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="041c38a6103440898124b090511d597a"
  ownershipid="AzureData_DataFactory" />
# Export and Import Resource Manager (ARM) Templates

## **Recommended Steps**
  * Use custom parameters with [Resource Manager template](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#use-custom-parameters-with-the-resource-manager-template
) to override default properties during deployment. You can now edit your arm-template-parameters-definition.json directly in ADF UX <br>
 * If you reach the Azure Resource Manager template size limits, use [Linked Resource Manager Templates](https://docs.microsoft.com//azure/data-factory/continuous-integration-deployment#linked-resource-manager-templates) to work around the limits. 

## **Recommended Documents**

* Export and Import ARM templates in data factory [Document](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#create-a-resource-manager-template-for-each-environment) <br>
* Copy or clone a data factory in ADF [Document](https://docs.microsoft.com/azure/data-factory/copy-clone-data-factory)
* Integrate into CI/CD cycle [Document](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment), including following sections: <br>

  * [Best practices](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#best-practices-for-cicd) _(please read)_ <br>
  * [Set up CI/CD releases with Git](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#continuous-integration-lifecycle) <br>
  * [Automate continuous integration](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#automate-continuous-integration-with-azure-pipelines-releases) with Azure Pipelines releases and [Deployment Template](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-deployment-template) <br>
  * Stop triggers before deployment and [restart them afterwards](https://docs.microsoft.com/azure/data-factory/continuous-integration-deployment#sample-script-to-stop-and-restart-triggers-and-clean-up) <br>