<properties
	pageTitle="Diagnose and resolve issues with Workspace"
	description="Diagnose and resolve issues with Workspace"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677733"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public"
	articleId="32507757-3fe2-45eb-9f0f-fd046dd47472"
/>

# Diagnose and resolve issues with Workspace

## **Recommended Documents**

* [Instances unreachable](https://kb.azuredatabricks.net/clusters/cluster-failed-launch.html#instances-unreachable)
* [How to Assign a Single Public IP for VNet-Injected Workspaces Using Azure Firewall](https://kb.azuredatabricks.net/cloud/azure-vnet-single-ip.html)
* Workspace deployment will fail, if you have used custom resource group name as a managed resource group. Custom resource group name should not exist within subscription.
* It is not possible to deploy two workspaces with same managed resource group name. If you tried to create 2 workspaces with the same managed resource group, it will fail.
* While deploying workspace though ARM Template, You can’t have Managed Resource Group Name as Existing Resource Group where workspace is present.
* If you are seeing the below error, please avoid having any special characters (- or _) as the first or last character in workspace name. Maximum length for Managed resource group Name : 1-90

```
{"status":"Failed","error":{"code":"ApplianceProvisioningFailed","message":"The provided resource group name 'parameters('nameManagedDatabricksResourceGroupRadar')' has these invalid characters: ''''. The name can only be a letter, digit, '-', '.', '(', ')' or '_'."}}
Please check if there are any invalid characters in Managed resource group name. Managed Resource Group Name should not have invalid characters. The name can only be a letter, digit, '-', '.', '(' ,  ')' or '_' ." . 
```


