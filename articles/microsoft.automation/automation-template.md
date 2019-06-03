<properties
    pageTitle="Azure Automation - ARM Template Deployment"
    description="Azure Automation - ARM Template Deployment"
    service="microsoft.automation"
    resource="automationaccounts"
    authors="rthorn17"
    ms.author="rithorn"
    displayorder=""
    selfHelpType="generic"
    articleId=""
    diagnosticScenario=""
    supportTopicIds="32641155"
    productPesIds="15607"
    cloudEnvironments="public"
/>

# Help with resolving ARM Template Deployment Issues

Here are some quick steps to some common Azure deployment errors:

## **Recommended Steps**

Review this article to locate your error code and gain insights into the issue [Troubleshoot common Azure deployment errors with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)

## Find error code

There are two types of errors you can receive:

* validation errors
* deployment errors

Validation errors arise from scenarios that can be determined before deployment. They include syntax errors in your template, or trying to deploy resources that would exceed your subscription quotas. Deployment errors arise from conditions that occur during the deployment process. They include trying to access a resource that is being deployed in parallel.

Both types of errors return an error code that you use to troubleshoot the deployment. Both types of errors appear in the [activity log](https://docs.microsoft.com/azure-resource-manager/resource-group-audit). However, validation errors don't appear in your deployment history because the deployment never started.

### Validation errors

When deploying through the portal, you see a validation error after submitting your values.

Select the message for more details. In the following image, you see an **InvalidTemplateDeployment** error and a message that indicates a policy blocked deployment.

### Deployment errors

When the operation passes validation, but fails during deployment, you get a deployment error.

To see deployment error codes and messages with PowerShell, use:

```azurepowershell-interactive
(Get-AzResourceGroupDeploymentOperation -DeploymentName exampledeployment -ResourceGroupName examplegroup).Properties.statusMessage
```

To see deployment error codes and messages with Azure CLI, use:

```azurecli-interactive
az group deployment operation list --name exampledeployment -g examplegroup --query "[*].properties.statusMessage"
```

In the portal, select the notification.

You see more details about the deployment. Select the option to find more information about the error.

You see the error message and error codes. Notice there are two error codes. The first error code (**DeploymentFailed**) is a general error that doesn't provide the details you need to solve the error. The second error code (**StorageAccountNotFound**) provides the details you need. 


## **Recommended Documents**

* [Troubleshoot common Azure deployment errors with Azure Resource Manager](https://docs.microsoft.com/azure/azure-resource-manager/resource-manager-common-deployment-errors)
* [Microsoft.Automation resource type template references](https://docs.microsoft.com/azure/templates/microsoft.automation/allversions)
* [Understand the structure and syntax of Azure Resource Manager templates](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-authoring-templates#quickstarts-and-tutorials)
* [Azure Resource Manager template best practices](https://docs.microsoft.com/azure/azure-resource-manager/template-best-practices)
* [Azure Resource Manager template functions](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-template-functions)
* [Using linked and nested templates when deploying Azure resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-linked-templates)
* [Develop Azure Resource Manager templates for cloud consistency](https://docs.microsoft.com/azure/azure-resource-manager/templates-cloud-consistency)
* [Azure Quickstart Templates](https://azure.microsoft.com/resources/templates/)

