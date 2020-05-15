<properties
	pageTitle="Post-Deployment Management Issues - Resource Locks"
	description="Post-Deployment Management Issues - Resource Locks"
	service="microsoft.solutions"
	resource="microsoft.solutions/application"
	authors="EvanHissey"
	ms.author="evanhi"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32628300"
	resourceTags=""
	productPesIds="16651"
	cloudEnvironments="public, fairfax, mooncake"	
    articleId="Post-DeploymentManagementIssues-Resourcelocks"
	ownershipId="Compute_AzureManagedApplications"
/>

# Resource Locks

Below are frequently asked questions and helpful links for understanding Resource Locks and resource access related to Service Catalog and Azure Managed Applications. <br>


## **I'm getting errors when trying to modify a resource within a managed application I deployed**

Managed applications deploy their underlying resources to a Managed Resource Group. You can find a managed application's associated managed resource group when viewing a managed application's essentials at the top of its Overview page. There you can find 'managed resource group' and a link to the resource group. <br>

## **Check if you have access to the managed application's resources**
If you did not author the Service Catalog Definition, or this managed application came from the Azure Marketplace, it's likely the resources within your managed application's managed resource group are locked to a different identity. You can view who has access to these resources by going the managed resource group, selecting 'Access control (IAM)' from the table of contents, selecting 'Role assignments' at the top, and viewing who has access and at what level to the resources. <br>


## **Modifying resources for a managed application's managed resource group that I manage**

To modify and update resources that are deployed as part of a managed application, you can directly change the resources found in a managed application's managed resource group. You can find a managed application's associated managed resource group when viewing a managed application's essentials at the top of its Overview page. There you can find 'managed resource group' and a link to the resource group.  <br>

## **Recommended Documents**

* [Modifying or updating resources in the managed resource group for an Azure managed application](https://docs.microsoft.com/azure/azure-resource-manager/managed-applications/update-managed-resources) <br>
* [Lock resources to prevent unexpected changes](https://docs.microsoft.com/azure/azure-resource-manager/management/lock-resources)
