<properties
  pagetitle="Azure pipelines issues while making use of Azure Resource Groups and ARM templates&#xD;"
  service="microsoft.visualstudio"
  resource="account"
  ms.author="v-abiss,cathmill"
  selfhelptype="Generic"
  supporttopicids="32742300"
  resourcetags=""
  productpesids="15543"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="azdevopspipelines"
  ownershipid="Azure_DevOps_Services" />
# Azure pipelines issues while making use of Azure Resource Groups and ARM templates

Resolve issues with Azure resource groups and ARM templates using the following recommendations.

## **Recommended Steps**

* **I get an error stating "The storage account is already taken"**

    The message indicates that the storage account name is already taken and applies specifically to the ARM template you are using. To find out if the name is already claimed, use [this API](https://docs.microsoft.com/rest/api/containerregistry/registries/checknameavailability).

* **I want to create and assign the Azure policy through Azure DevOps without using third-party tasks**

   Assign the policies with an [ARM template](https://docs.microsoft.com/azure/governance/policy/assign-policy-template), or make use of [Azure Cli task](https://docs.microsoft.com/azure/governance/policy/assign-policy-azurecli) and [Azure PowerShell task](https://docs.microsoft.com/azure/governance/policy/assign-policy-powershell) respectively.

* **The KeyVault can't be deployed through ARM template in the Azure portal using Azure DevOps pipeline and returns the error: "Bad JSON content found in the request"**

    Find the line of code in the ARM template that contains the Tenant ID and replace the **Subscription().TenantId** with the **actual Tenant ID**. Also, you can [create a secret variable in the pipeline](https://docs.microsoft.com/azure/devops/pipelines/process/variables?view=azure-devops&tabs=yaml%2Cbatch) for the **Tenant ID** and pass the variable in the ARM template.

* **I'm facing an SPN permission issue with the ARM template**

    The Service Principal must have either a [**User Access Administrator** or **Owner** rights](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-powershell#prerequisites%20[docs.microsoft.com])


## **Recommended Documents**

* [Best practices](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-best-practices)
* [Create and Deploy an ARM template](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-create-first-template?tabs=azure-powershell)
* [Export template from a resource group](https://docs.microsoft.com/azure/azure-resource-manager/templates/export-template-portal)
* [Integrate ARM templates with Azure Pipelines](https://docs.microsoft.com/azure/azure-resource-manager/templates/add-template-to-azure-pipelines)
* [Continuous integration of Azure Resource Manager templates with Azure Pipelines](https://docs.microsoft.com/azure/azure-resource-manager/templates/deployment-tutorial-pipeline)
* [Create a policy assignment to identify non-compliant resources by using an ARM template](https://docs.microsoft.com/azure/governance/policy/assign-policy-template)
* For service-impacting issues, see [Azure DevOps Services Status](https://status.dev.azure.com/)
* Want a quicker answer? For quick answers to common questions and issues, try the [Azure DevOps Virtual Agent](https://azuredevopsvirtualagent.azurewebsites.net/)
