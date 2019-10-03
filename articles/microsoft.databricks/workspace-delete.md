<properties
	pageTitle="Diagnose and resolve issues with Workspace delete"
	description="Diagnose and resolve issues with Workspace delete"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677734"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="178b9906-c5b3-4eed-9a7a-dac993391ade"
/>

# Diagnose and resolve issues with Workspace deletion

## **Recommended Steps**

* Steps to delete workspace:
     * Login to portal and navigate to Databricks Workspace that needs to be deleted
     * Click on Managed Resource Group 
     * Click 'delete' to delete Managed Resource Group, after confirming there are no [locks](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-lock-resources#managed-applications-and-locks)
     * Once Managed Resource group deletion is successful, proceed with deleting workspace
     
     
* Cleanup of workspace is an asynchronous process and takes about 5-10 minutes to clean up cluster resources like VNET, Virtual Machines, storage and NSG.  If you just initiated it, please check after 5-10 minutes.
