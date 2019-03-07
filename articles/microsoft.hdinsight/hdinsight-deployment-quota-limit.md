<properties
    pageTitle="HDInsight deployment quota limitation"
    description="Exceeded the HDInsight deployment quota per resource group."
    infoBubbleText="Exceeded deployment quota. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="mahariha"
    ms.author="mahariha"
    displayOrder=""
    articleId="Hdi_Crud_ExceededDeploymentQuota"
    diagnosticScenario="HDInsightExceededDeploymentQuotaInsight"
    selfHelpType="rca"
    supportTopicIds="32628987, 32629125, 32629032"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

You have reached the limit on the maximum number of deployments allowed per resource group. Current deployment quota is <!--$DeploymentQuota-->[DeploymentQuota]<!--/$DeploymentQuota-->. Please delete deployments that are no longer needed from the history of resource group '<!--$ResourceGroup-->[ResourceGroup]<!--/$ResourceGroup-->' to resolve the issue. 

## **Recommended Steps**

You can cleanup the deployment history using one of the following methods.

## Delete deployments using Portal.

1. Login to portal and navigate to the resource group <!--$ResourceGroup-->[ResourceGroup]<!--/$ResourceGroup-->.
2. Select 'Deployments' from the resource group. 
3. Select and delete the deployments that are no longer needed.

### Delete deployments using PowerShell.
	
1. Open powershell.
2. Login to the subscription and run the following command.
`Get-AzureRmResourceGroupDeployment -ResourceGroupName <!--$ResourceGroup-->[ResourceGroup]<!--/$ResourceGroup--> |  Where-Object {$_.DeploymentName -like "*parentdeployment*" -or $_.DeploymentName -like "*subdeployment*"} | Where-Object {$_.Timestamp -lt (get-date).AddDays(-5)} | Where-Object {$_.ProvisioningState -like "Succeeded"} | Remove-AzureRmResourceGroupDeployment -ResourceGroupName <!--$ResourceGroup-->[ResourceGroup]<!--/$ResourceGroup--> -Name { $_.DeploymentName } -ErrorAction SilentlyContinue`

### Periodic deletion using Runbook.

* You can also setup a scheduled [Runbook within Azure Automation](https://docs.microsoft.com/en-us/azure/automation/start-runbooks) to execute a powershell script to periodically clean out the stored Resource Group Deployments. Refer the documentation [Handling Azure Resource Manager Deployment Limits](https://blogs.msdn.microsoft.com/cloud_solution_architect/2016/08/22/handling-azure-resource-manager-deployment-limits) for more information.

## **Recommended Documents**

* [Azure subscription and service limits, quotas, and constraints](https://azure.microsoft.com/en-us/documentation/articles/azure-subscription-service-limits/)
* [Handling Azure Resource Manager Deployment Limits](https://blogs.msdn.microsoft.com/cloud_solution_architect/2016/08/22/handling-azure-resource-manager-deployment-limits)
* [Start a runbook in Azure Automation](https://docs.microsoft.com/en-us/azure/automation/start-runbooks)
	