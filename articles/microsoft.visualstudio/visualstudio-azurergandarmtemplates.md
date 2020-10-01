<properties
	pageTitle="Azure Resource Groups and ARM templates"
	description="Issues related to template deployments like template validation error, resources not found or any guidance with the configuration"
	infoBubbleText="Azure Pipelines issues related to script execution through both PowerShell & Azure CLI"
	service="microsoft.visualstudio"
	resource="account"
	authors="v-abiss"
	ms.author="v-abiss"
	articleId="AZDevOpsPipelines"
	supportTopicIds="32742300"
	diagnosticScenario=""
	selfHelpType="generic"
	resourceTags=""
	productPesIds="15543"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="Azure_DevOps_Services"
/>

# Azure pipelines issues while making use of Azure PowerShell & Azure CLI

## **Recommended Steps**

Are you facing one of these common problems?

* I get an error stating "The storage account is already taken"

    The error seems to be an issue with the ARM template which you are using and the message clearly says that the storage account name is already taken. You can check if the name is already claimed by using [this API](https://docs.microsoft.com/rest/api/containerregistry/registries/checknameavailability).

* I want to create and assign the Azure policy through Azure DevOps without having to use third-party tasks

    You can either use an [ARM template](https://docs.microsoft.com/azure/governance/policy/assign-policy-template) to assign the policies or make use of [Azure Cli task](https://docs.microsoft.com/azure/governance/policy/assign-policy-azurecli) and [Azure PowerShell task](https://docs.microsoft.com/azure/governance/policy/assign-policy-powershell) respectively.

* The KeyVault can't be deployed through ARM template in portal using Azure DevOps pipeline as it gives the error: **""Bad JSON content found in the request"**

    Check the line of code in the ARM template which contains the Tenant ID and replace the Subscription().TenantId with the **actual Tenant ID**. Also, you can [create a secret variable in the pipeline](https://docs.microsoft.com/azure/devops/pipelines/process/variables?view=azure-devops&tabs=yaml%2Cbatch) for the **Tenant ID** and pass the variable in the ARM template.

* I'm facing an SPN permission issue with the ARM template

    The Service Principal must have either a **User Access Administrator** or **Owner** rights. [Refer this document](https://docs.microsoft.com/azure/role-based-access-control/role-assignments-powershell#prerequisites%20[docs.microsoft.com])


## **Recommended Documents**

* [Best practices](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-best-practices)
* [Create and Deploy an ARM template](https://docs.microsoft.com/azure/azure-resource-manager/templates/template-tutorial-create-first-template?tabs=azure-powershell)
* [Export template from a resource group](https://docs.microsoft.com/azure/azure-resource-manager/templates/export-template-portal)
* [Integrate ARM templates with Azure Pipelines](https://docs.microsoft.com/azure/azure-resource-manager/templates/add-template-to-azure-pipelines)
* [Continuous integration of Azure Resource Manager templates with Azure Pipelines](https://docs.microsoft.com/azure/azure-resource-manager/templates/deployment-tutorial-pipeline)
* [Create a policy assignment to identify non-compliant resources by using an ARM template](https://docs.microsoft.com/azure/governance/policy/assign-policy-template)
