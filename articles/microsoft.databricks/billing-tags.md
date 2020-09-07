<properties
	pageTitle="Diagnose and resolve issues with Databricks Tags"
	description="Diagnose and resolve issues with Databricks Tags"
	service="microsoft.databricks"
	resource="workspaces"
	authors="deeptivu"
	ms.author="deeptivu"
	displayOrder="15"
	selfHelpType="generic"
	supportTopicIds="32677730"
	resourceTags=""
	productPesIds="16432"
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="50078350-c098-4986-bd32-ec5c3f9e5618"
	ownershipId="AzureData_AzureDatabricks"
/>

# Diagnose and resolve issues with Databricks Tags

## **Recommended Steps**

* [Use tags to organize your Azure resources](https://docs.microsoft.com/azure/azure-resource-manager/resource-group-using-tags)
* By design, tags cannot be added to a managed resource group. Instead, please create tags to Workspace, which will eventually propagate to Managed Resource Group tags. Tags can be added to [ARM template](https://github.com/Azure/azure-quickstart-templates/tree/master/101-databricks-workspace). Please add Tag to "resources":

```
"resources": [
{
"type": "Microsoft.Databricks/workspaces",
"name": "[parameters('workspaceName')]",
"location": "[parameters('location')]",
"apiVersion": "2018-04-01",
"sku": {
"name": "[parameters('pricingTier')]"
},
"tags": {
"<Name1>": "<Value1>",
"<Name2>": "<Value2>"
}
"properties": {
"ManagedResourceGroupId": "[concat(subscription().id, '/resourceGroups/', variables('managedResourceGroupName'))]"
}
}
]
```

**Note**: Today Tags created at workspace are not propagated to Databricks Cluster resources. Same tag needs to be manually created from Databricks Cluster configuration page, as explained [here](https://docs.databricks.com/user-guide/clusters/tags.html).
