<properties
	pageTitle="Customer subscription too many deployments"
	description="Customer subscription too many deployments"
    service="Microsoft.HDInsight"
    resource="Microsoft.HDInsight/clusters"
	authors="Jacky-hdi"
	ms.author="linjzhu"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="890c864c-ed25-4813-90c6-be26af7a7b23"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Customer subscription too many deployments

<!--issueDescription-->

We have checked the cluster and this failure is high likely that HDI cluster deployments hit the quota limit of 800 in  ***{ResourceGroupName}***.

<!--/issueDescription-->

To resolve the issue:

- From portal
1. login the portal and navigate to the issue resource group
2. select 'Deployments' from the resource group
3. delete the old deployments and recreate again

- From powershell
1. run the below powershell to check and delete old deployments
```powershell
Login-AzureRmAccount -SubscriptionId <usersubscriptionId>
Get-AzureRmResourceGroupDeployment -ResourceGroupName <ResourceGroupName> | measure
Remove-AzureRmResourceGroupDeployment -ResourceGroupName <ResourceGroupName> -Name <userdeploymentname> -ErrorAction SilentlyContinue
```
2. recreate the cluster again

## **Recommended Documents**

* [Resource Group Limits](https://docs.microsoft.com/en-us/azure/azure-resource-manager/management/azure-subscription-service-limits#resource-group-limits)

